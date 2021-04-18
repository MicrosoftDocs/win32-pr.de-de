---
description: Eine Möglichkeit zum Erstellen von frei Hand fähigen Webanwendungen besteht darin, innerhalb von Microsoft Internet Explorer Windows Forms Steuerelemente in awebpagezu platzieren.
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Websteuer Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b28fa2a3293b6b780412ddbc755634c745b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343285"
---
# <a name="web-controls"></a>Websteuer Elemente

Eine Möglichkeit zum Erstellen von frei Hand fähigen Webanwendungen besteht darin, innerhalb von Microsoft Internet Explorer Windows Forms Steuerelemente in awebpagezu platzieren. Ein gutes Tutorial zu diesem Verfahren finden Sie unter Verwenden von Windows Forms-Steuer [Elementen in Internet Explorer](https://windowsclient.net/articles/iesourcing.aspx). Die grundlegenden Schritte im Tutorial lauten wie folgt:

1.  Erstellen Sie ein Steuerelement, das von [**System. Windows. Forms. UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)erbt.
2.  Erstellen Sie eine HTML-Seite mit einem Objekttag, das auf das UserControl-Steuerelement verweist.
3.  Erstellen Sie ein virtuelles Verzeichnis, und legen Sie Berechtigungen fest.
4.  Laden Sie die URL der HTML-Seite in den Browser.

Diese Technik kann auf Freihand-aktivierte Steuerelemente wie jedes andere Windows Forms [**Steuer**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)Element angewendet werden. Tatsächlich kann die Technik mit jeder Klasse im Microsoft .NET Framework verwendet werden. Die vom Microsoft Windows XP Tablet PC Edition-SDK (Software Development Kit) bereitgestellten Beispiele beinhalten eine websteuerungs Version des Beispiels "Auto Claims" im Abschnitt "Ink Web Samples". In diesem Beispiel wird das ursprüngliche [Formular Beispiel für automatische Ansprüche](auto-claims-form-sample.md) übernommen und in ein Steuerelement umgewandelt, das auf einer Webseite abgelegt ist. Weitere Informationen zur Webaktivierung dieses Beispiels finden Sie im Beispiel für das [Ink-websteuer](ink-web-control-sample.md)Element.

> [!Note]  
> Wenn Sie eine Anwendung bereitstellen, die mithilfe von .net über das Internet erstellt wurde, kann die Anwendung vom Sicherheitsmodell für .net betroffen sein. Weitere Informationen zur Funktionsweise der Sicherheit mit frei Hand fähigen Webanwendungen finden Sie unter [Sicherheit und Vertrauens](security-and-trust.md)Stellung.

 

 

 
