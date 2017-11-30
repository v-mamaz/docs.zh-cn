---
title: "ICorDebugProcess::ClearCurrentException 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugProcess.ClearCurrentException
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugProcess::ClearCurrentException
helpviewer_keywords:
- ClearCurrentException method, ICorDebugProcess interface [.NET Framework debugging]
- ICorDebugProcess::ClearCurrentException method [.NET Framework debugging]
ms.assetid: 9e02ee1a-e495-4578-bfb5-b946274bede7
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 8c6204f8906a29f7e8541d548872b6e84fd883bb
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugprocessclearcurrentexception-method"></a><span data-ttu-id="50fd7-102">ICorDebugProcess::ClearCurrentException 方法</span><span class="sxs-lookup"><span data-stu-id="50fd7-102">ICorDebugProcess::ClearCurrentException Method</span></span>
<span data-ttu-id="50fd7-103">清除在给定的线程上当前的非托管的异常。</span><span class="sxs-lookup"><span data-stu-id="50fd7-103">Clears the current unmanaged exception on the given thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50fd7-104">语法</span><span class="sxs-lookup"><span data-stu-id="50fd7-104">Syntax</span></span>  
  
```  
HRESULT ClearCurrentException([in] DWORD threadID);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="50fd7-105">参数</span><span class="sxs-lookup"><span data-stu-id="50fd7-105">Parameters</span></span>  
 `threadID`  
 <span data-ttu-id="50fd7-106">[in]将在其清除当前的非托管的异常的线程 ID。</span><span class="sxs-lookup"><span data-stu-id="50fd7-106">[in] The ID of the thread on which the current unmanaged exception will be cleared.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="50fd7-107">备注</span><span class="sxs-lookup"><span data-stu-id="50fd7-107">Remarks</span></span>  
 <span data-ttu-id="50fd7-108">调用此方法之前调用[icordebugcontroller:: Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md)时线程已报告应忽略的调试对象的非托管的异常。</span><span class="sxs-lookup"><span data-stu-id="50fd7-108">Call this method before calling [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) when a thread has reported an unmanaged exception that should be ignored by the debuggee.</span></span> <span data-ttu-id="50fd7-109">这将清除的未完成的带内 (IB) 和在给定的线程上的带外 (OOB) 事件。</span><span class="sxs-lookup"><span data-stu-id="50fd7-109">This will clear both the outstanding in-band (IB) and out-of-band (OOB) events on the given thread.</span></span> <span data-ttu-id="50fd7-110">自动清除所有 OOB 断点和单步执行的异常。</span><span class="sxs-lookup"><span data-stu-id="50fd7-110">All OOB breakpoints and single-step exceptions are automatically cleared.</span></span>  
  
 <span data-ttu-id="50fd7-111">使用[icordebugthread2:: Interceptcurrentexception](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-interceptcurrentexception-method.md)截获当前托管线程上的异常。</span><span class="sxs-lookup"><span data-stu-id="50fd7-111">Use [ICorDebugThread2::InterceptCurrentException](../../../../docs/framework/unmanaged-api/debugging/icordebugthread2-interceptcurrentexception-method.md) to intercept the current managed exception on a thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="50fd7-112">要求</span><span class="sxs-lookup"><span data-stu-id="50fd7-112">Requirements</span></span>  
 <span data-ttu-id="50fd7-113">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="50fd7-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="50fd7-114">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="50fd7-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="50fd7-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="50fd7-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="50fd7-116">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="50fd7-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>