---
title: "如何： 获取和设置应用程序主窗口"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- windows objects [WPF], setting
- setting windows objects [WPF]
- windows objects [WPF], getting
- getting windows objects [WPF]
ms.assetid: ec902bc4-4a59-46f5-8ec1-963b46789356
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 0d6bca158172fd3fc31526287c6d4a9928a8ea0c
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/22/2017
---
# <a name="how-to-get-and-set-the-main-application-window"></a><span data-ttu-id="bb963-102">如何： 获取和设置应用程序主窗口</span><span class="sxs-lookup"><span data-stu-id="bb963-102">How to: Get and Set the Main Application Window</span></span>
<span data-ttu-id="bb963-103">此示例演示如何获取和设置应用程序主窗口。</span><span class="sxs-lookup"><span data-stu-id="bb963-103">This example shows how to get and set the main application window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bb963-104">示例</span><span class="sxs-lookup"><span data-stu-id="bb963-104">Example</span></span>  
 <span data-ttu-id="bb963-105">第一个<xref:System.Windows.Window>中实例化的[!INCLUDE[TLA#tla_wpf](../../../../includes/tlasharptla-wpf-md.md)]应用程序自动通过设置<xref:System.Windows.Application>作为主应用程序窗口。</span><span class="sxs-lookup"><span data-stu-id="bb963-105">The first <xref:System.Windows.Window> that is instantiated within a [!INCLUDE[TLA#tla_wpf](../../../../includes/tlasharptla-wpf-md.md)] application is automatically set by <xref:System.Windows.Application> as the main application window.</span></span> <span data-ttu-id="bb963-106">第一个<xref:System.Windows.Window>要实例化的将最可能是指定为启动窗口[!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)](请参阅<xref:System.Windows.Application.StartupUri%2A>)。</span><span class="sxs-lookup"><span data-stu-id="bb963-106">The first <xref:System.Windows.Window> to be instantiated will most likely be the window that is specified as the startup [!INCLUDE[TLA#tla_uri](../../../../includes/tlasharptla-uri-md.md)] (see <xref:System.Windows.Application.StartupUri%2A>).</span></span>  
  
 <span data-ttu-id="bb963-107">第一个<xref:System.Windows.Window>也无法使用代码来实例化。</span><span class="sxs-lookup"><span data-stu-id="bb963-107">The first <xref:System.Windows.Window> could also be instantiated using code.</span></span> <span data-ttu-id="bb963-108">一个示例应用程序在启动期间，如下所示打开一个窗口：</span><span class="sxs-lookup"><span data-stu-id="bb963-108">One example is opening a window during application startup, like the following:</span></span>  
  
 [!code-csharp[HOWTOWindowManagementSnippets#FirstWindowUsingCodeCODEBEHIND](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/App.xaml.cs#firstwindowusingcodecodebehind)]
 [!code-vb[HOWTOWindowManagementSnippets#FirstWindowUsingCodeCODEBEHIND](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/application.xaml.vb#firstwindowusingcodecodebehind)]  
  
 <span data-ttu-id="bb963-109">有时，第一个实例化<xref:System.Windows.Window>是不实际应用程序主窗口，例如初始屏幕。</span><span class="sxs-lookup"><span data-stu-id="bb963-109">Sometimes, the first instantiated <xref:System.Windows.Window> is not actually the main application window e.g. a splash screen.</span></span> <span data-ttu-id="bb963-110">在这种情况下，你可以指定主应用程序窗口使用标记，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bb963-110">In this case, you can specify the main application window using markup, like the following:</span></span>  
  
 [!code-xaml[ApplicationMainWindowSnippets#SetApplicationMainWindowXAML](../../../../samples/snippets/xaml/VS_Snippets_Wpf/ApplicationMainWindowSnippets/XAML/App.xaml#setapplicationmainwindowxaml)]  
  
 <span data-ttu-id="bb963-111">是否自动或手动指定主窗口，则你可以从主窗口<xref:System.Windows.Application.MainWindow%2A>使用下面的代码，如下所示：</span><span class="sxs-lookup"><span data-stu-id="bb963-111">Whether the main window is specified automatically or manually, you can get the main window from <xref:System.Windows.Application.MainWindow%2A> using the following code, like the following:</span></span>  
  
 [!code-csharp[ApplicationMainWindowSnippets#GetApplicationMainWindowCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ApplicationMainWindowSnippets/CSharp/App.xaml.cs#getapplicationmainwindowcode)]
 [!code-vb[ApplicationMainWindowSnippets#GetApplicationMainWindowCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ApplicationMainWindowSnippets/visualbasic/application.xaml.vb#getapplicationmainwindowcode)]