---
description: In diesem Beispiel wird gezeigt, wie Sie eine verwaltete Tablet PC-Anwendung über das Internet mithilfe der No-Touchscreen-Bereitstellung bereitstellen.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: No-Touch Bereitstellungs-webbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0742deef8ea9b418fba6de4724975ee27693f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530443"
---
# <a name="no-touch-deployment-web-sample"></a>No-Touch Bereitstellungs-webbeispiel

In diesem Beispiel wird gezeigt, wie Sie eine verwaltete Tablet PC-Anwendung über das Internet mithilfe der No-Touchscreen-Bereitstellung bereitstellen. Sie sollten sich mit den Konzepten vertraut machen, die in [der .NET Framework bereit](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp)gestellt werden. Auf dem Computer muss Microsoft Internetinformationsdienste (IIS) installiert sein, um dieses Beispiel ausführen zu können.

## <a name="overview"></a>Übersicht

Bei der Bereitstellung ohne Fingereingabe können Tablet PCWindows Forms-Anwendungen-Desktop Anwendungen, die mithilfe der Klassen im System. Windows. Forms-Namespace von Microsoft .NET Framework und Microsoft Windows XP Tablet PC Edition Development Kit 1,7 erstellt wurden, heruntergeladen, installiert und direkt auf den Computern der Benutzer ausgeführt werden, ohne dass die Registrierung oder die freigegebenen System Komponenten geändert werden müssen.

In diesem Beispiel wird das ursprüngliche Projekt für das [Formular Beispiel "Automatische Ansprüche](auto-claims-form-sample.md)", "autoclaims" und ein Installer-Projekt, "autoclaims \_ notouchweb", bereitstellt. Nachdem Sie kompiliert und ausgeführt wurden, erstellt das Installer-Projekt ein neues virtuelles Stammverzeichnis, das auch autoclaims \_ notouchweb genannt wird. Das Installationsprogramm kopiert eine Datei default.htm, die einen Link zur AutoClaims.exe Assembly enthält. Navigieren Sie zum Starten der Rich Client-Anwendung mit Microsoft Internet Explorer zum virtuellen Stammverzeichnis, und klicken Sie dann auf der Seite default.htm auf den Link.

> [!Note]  
> Zum virtuellen Stammverzeichnis müssen Sie IIS (z. b. https://localhost/AutoClaims\_NoTouchWeb/default.htm) und nicht direkt über das Dateisystem) navigieren, damit die Anwendung in der Internet Explorer-Anwendungsdomäne funktioniert.

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a>No-Touch Bereitstellungs Anforderungen

Alle abhängigen Assemblys müssen sich entweder im Assemblysuchpfad oder im Stammverzeichnis des virtuellen Verzeichnisses der Website befinden. Das \_ Bereitstellungs Projekt "autoclaims notouchweb" installiert die Assembly und die verweisende Seite (default.htm) im selben virtuellen Stammverzeichnis (autoclaims \_ notouchweb).

> [!Note]  
> Die kompilierten webbeispiele werden von der Standard Installationsoption für das SDK nicht installiert. Sie müssen eine benutzerdefinierte Installation durchführen und die unter Option "vorkompilierte webbeispiele" auswählen, um Sie zu installieren.

 

Weitere Informationen zur Verwendung von frei Hand Eingaben im Web finden Sie unter frei Hand Eingaben [im Web](ink-on-the-web.md).

 

 