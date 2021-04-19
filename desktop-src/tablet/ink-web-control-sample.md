---
description: In diesem Beispiel wird gezeigt, wie ein frei Hand fähiges Steuerelement für die Verwendung in einem Webbrowser erstellt wird. Im Beispiel wird das ursprüngliche Formular Beispiel für automatische Ansprüche übernommen und in ein Steuerelement umgewandelt, das auf einer Webseite abgelegt ist.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Ink-websteuer Element-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101537c4cc7b42181cf8d9ff177a5854c5b84054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353059"
---
# <a name="ink-web-control-sample"></a>Ink-websteuer Element-Beispiel

In diesem Beispiel wird gezeigt, wie ein frei Hand fähiges Steuerelement für die Verwendung in einem Webbrowser erstellt wird. Im Beispiel wird das ursprüngliche [Formular Beispiel für automatische Ansprüche](auto-claims-form-sample.md) übernommen und in ein Steuerelement umgewandelt, das auf einer Webseite abgelegt ist.

Weitere Informationen zur Verwendung von frei Hand Eingaben im Web finden Sie unter frei Hand Eingaben [im Web](ink-on-the-web.md).

## <a name="modifications-to-the-original-sample-project"></a>Änderungen am ursprünglichen Beispiel Projekt

Dieses Beispiel besteht aus einer Projekt Mappe, die zwei Projekte und eine HTML-Datei enthält. Das erste Projekt, autoclaims, ist ein Microsoft Visual C- \# Steuerelement Bibliothek-Projekt (ein Benutzer Steuerelement). Der Quellcode für dieses Steuerelement ist beinahe identisch mit dem des Beispiels "autoclaims" mit zwei unterschieden:

-   Die- `AutoClaims` Klasse in diesem Beispiel erbt von der [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) -Klasse und nicht von der [Formular](/dotnet/api/system.windows.forms.form?view=netcore-3.1) Klasse.

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   Die autoclaims-Klasse in diesem Beispiel verfügt über eine hinzugefügte öffentliche Methode, die die internen untergeordneten Steuer `DisposeResources` Elemente zum Sammeln von frei Hand Eingaben freigibt. Diese Methode muss von der Webpage aufgerufen werden, die das-Steuerelement verwendet, wenn diese Seite die Verwendung des-Steuer Elements beendet.

## <a name="referencing-the-control-in-html"></a>Verweisen auf das Steuerelement in HTML

Die Lösung enthält eine HTML-Datei, default.htm. Diese Datei ist die Seite, zu der der Browser navigiert, um das Steuerelement zu laden. Die Datei enthält ein- <object> Tag, das auf das-Steuerelement verweist. Sie enthält auch ein Skript, das aufgerufen wird, wenn die Seite entladen wird, wie durch das vorhanden sein des OnLoad = " `OnUnload()` "-Attributs im <body> ein. Diese Funktion Ruft die-Methode des-Steuer Elements auf `DisposeResources` , um sicherzustellen, dass alle Ressourcen beim Herunterfahren ordnungsgemäß freigegeben werden.


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



Beachten Sie das Format des ClassID-Attribut Werts für das <object> Tag. Sie benennt die Assembly, gefolgt von einem \# Vorzeichen Trennzeichen, und dann den Namespace, der das Steuerelement enthält, und dann den Klassennamen des Steuer Elements.

Ein Benutzer Steuerelement in der Praxis würde wahrscheinlich zusätzliche Methoden enthalten, mit denen die in der Anwendung gesammelten Daten persistent gespeichert oder gesendet werden.

## <a name="the-autoclaims_webcontrol-project"></a>Das Projekt autoclaims \_ WebControl

Das Projekt autoclaims \_ WebControl ist ein Bereitstellungs Projekt, das ein-Setup erstellt, das bei der Installation ein virtuelles Stammverzeichnis, autoclaims \_ WebControl, auf dem Webserver hinzufügt. Das-Steuerelement und die HTML-Datei werden in diesem virtuellen Stammverzeichnis platziert.

> [!Note]  
> Die kompilierten webbeispiele werden von der Standard Installationsoption für das SDK nicht installiert. Sie müssen eine benutzerdefinierte Installation durchführen und die unter Option "vorkompilierte webbeispiele" auswählen, um Sie zu installieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel für automatisches Anspruchsformular](auto-claims-form-sample.md)
</dt> <dt>

[Frei Hand Eingaben im Web](ink-on-the-web.md)
</dt> </dl>

 

 
