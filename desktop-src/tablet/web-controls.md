---
description: Eine Möglichkeit zum Erstellen von Ink-fähigen Webanwendungen besteht darin, Windows Forms-Steuerelemente in einerwebpagewithin Microsoft-Internet Explorer.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Websteuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3abd7dd40bdeed36bff437e76d2e2aeaa64688f89a0d3bafff34ee8314833b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041692"
---
# <a name="web-controls"></a>Websteuerelemente

Eine Möglichkeit zum Erstellen von Ink-fähigen Webanwendungen besteht darin, Windows Forms-Steuerelemente in einerwebpagewithin Microsoft-Internet Explorer. Ein gutes Tutorial zu dieser Technik finden Sie unter [Verwenden von Windows Forms-Steuerelementen in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx). Die grundlegenden Schritte im Tutorial sind:

1.  Erstellen Sie ein Steuerelement, das von [**System.Windows. Forms.UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1).
2.  Erstellen Sie eine HTML-Seite mit einem Objekttag, das auf dieses UserControl verweist.
3.  Erstellen Sie ein virtuelles Verzeichnis, und legen Sie Berechtigungen fest.
4.  Laden Sie die URL der HTML-Seite in den Browser.

Diese Technik kann auf ink-fähige Steuerelemente angewendet werden, genau wie jedes andere Windows [**Forms-Steuerelement.**](/dotnet/api/system.windows.forms.control?view=netcore-3.1) Tatsächlich kann die Technik mit jeder Klasse im Microsoft-.NET Framework. Die vom Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) bereitgestellten Beispiele enthalten eine Websteuersatzversion des Beispiels für automatische Ansprüche im Abschnitt Ink-Webbeispiele. In diesem Beispiel wird das ursprüngliche [Formularbeispiel](auto-claims-form-sample.md) für automatische Ansprüche in ein Steuerelement geändert, das auf einer Webseite gespeichert wird. Weitere Informationen zur Web-Aktivierung dieses Beispiels finden Sie unter [Ink Web Control Sample](ink-web-control-sample.md).

> [!Note]  
> Wenn Sie eine Anwendung bereitstellen, die mithilfe von .NET über das Web erstellt wurde, kann das Sicherheitsmodell für .NET die Anwendung beeinflusst. Weitere Informationen zur Funktionsweise der Sicherheit bei Ink-fähigen Webanwendungen finden Sie unter [Sicherheit und Vertrauenswürdigkeit.](security-and-trust.md)

 

 

 
