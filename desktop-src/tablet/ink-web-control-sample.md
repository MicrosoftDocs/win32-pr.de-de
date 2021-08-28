---
description: In diesem Beispiel wird gezeigt, wie Sie ein Steuerelement mit Ink-Aktivierung für die Verwendung in einem Webbrowser erstellen. Das Beispiel verwendet das ursprüngliche Formularbeispiel für automatische Ansprüche und wandelt es in ein Steuerelement um, das auf einer Webseite angezeigt wird.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Beispiel für Ink-Websteuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe2035028ab622f896489b304ca850db4e25462
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882046"
---
# <a name="ink-web-control-sample"></a>Beispiel für Ink-Websteuerelement

In diesem Beispiel wird gezeigt, wie Sie ein Steuerelement mit Ink-Aktivierung für die Verwendung in einem Webbrowser erstellen. Das Beispiel verwendet das ursprüngliche [Formularbeispiel](auto-claims-form-sample.md) für automatische Ansprüche und wandelt es in ein Steuerelement um, das auf einer Webseite angezeigt wird.

Weitere Informationen zur Verwendung von Ink im Web finden Sie unter [Ink im Web.](ink-on-the-web.md)

## <a name="modifications-to-the-original-sample-project"></a>Änderungen am ursprünglichen Beispiel Project

Dieses Beispiel besteht aus einer Projektmappe, die zwei Projekte und eine HTML-Datei enthält. Das erste Projekt, AutoClaims, ist ein Microsoft Visual \# C-Steuerelementbibliotheksprojekt (ein Benutzersteuerelement). Der Quellcode für dieses Steuerelement ist fast identisch mit dem des AutoClaims-Beispiels mit zwei Unterschieden:

-   Die `AutoClaims` -Klasse in diesem Beispiel erbt von der [UserControl-Klasse](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) und nicht von der [Form-Klasse.](/dotnet/api/system.windows.forms.form?view=netcore-3.1)

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   Die AutoClaims-Klasse in diesem Beispiel verfügt über eine hinzugefügte öffentliche Methode, mit der die internen untergeordneten Steuerelemente verworfen `DisposeResources` werden, die zum Sammeln von Freihanddaten verwendet werden. Diese Methode muss von derwebpage aufgerufen werden, auf der das -Steuerelement verwendet wird, wenn diese Seite mit dem -Steuerelement beendet ist.

## <a name="referencing-the-control-in-html"></a>Verweisen auf das Steuerelement in HTML

Die Projektmappe enthält eine HTML-Datei default.htm. Diese Datei ist die Seite, zu der der Browser navigiert, um das Steuerelement zu laden. Die Datei enthält ein &lt; &gt; Objekttag, das auf das Steuerelement verweist. Es enthält auch ein Skript, das aufgerufen wird, wenn die Seite entladen wird, wie durch das Vorhandensein des onload=" `OnUnload()` " -Attributs im &lt; &gt; Texttag angegeben. Diese Funktion ruft die `DisposeResources` -Methode für das -Steuerelement auf, um sicherzustellen, dass alle Ressourcen beim Herunterfahren ordnungsgemäß freigegeben werden.


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



Beachten Sie das Format des classid-Attributwerts für das &lt; &gt; Objekttag. Er benennt die Assembly, gefolgt von einem \# Vorzeichentrennzeichen und dann den Namespace, der das Steuerelement enthält, und dann den Klassennamen des Steuerelements.

Ein echtes Benutzersteuerelement würde wahrscheinlich zusätzliche Methoden enthalten, die zum Beibehalten oder Senden der in der Anwendung gesammelten Daten verwendet werden.

## <a name="the-autoclaims_webcontrol-project"></a>AutoClaims \_ WebControl-Project

Das AutoClaims \_ WebControl-Projekt ist eine Bereitstellungs-Project, die ein Setup erstellt, das bei der Installation ein virtuelles Stammverzeichnis (AutoClaims \_ WebControl) auf dem Webserver hinzufügt. Das Steuerelement und die HTML-Datei werden in diesem virtuellen Stamm abgelegt.

> [!Note]  
> Die kompilierten Webbeispiele werden nicht von der Standardinstallationsoption für das SDK installiert. Sie müssen eine benutzerdefinierte Installation abschließen und die Unteroption "Vorkompilierte Webbeispiele" auswählen, um sie zu installieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel für das Formular für automatische Ansprüche](auto-claims-form-sample.md)
</dt> <dt>

[Ink im Web](ink-on-the-web.md)
</dt> </dl>

 

 
