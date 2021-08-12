---
description: In diesem Beispiel wird gezeigt, wie Sie eine verwaltete Tablet PC-Anwendung über das Web bereitstellen, indem Sie die No-Touch-Bereitstellung verwenden.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: No-Touch Deployment Web Sample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d8fb9989785dc081022c2e76d8fade6d48bf521b3f27449ff5aac963706f356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449651"
---
# <a name="no-touch-deployment-web-sample"></a>No-Touch Deployment Web Sample

In diesem Beispiel wird gezeigt, wie Sie eine verwaltete Tablet PC-Anwendung über das Web bereitstellen, indem Sie die No-Touch-Bereitstellung verwenden. Sie sollten mit den Konzepten vertraut sein, die unter [No-Touch Deployment (No-Touch-Bereitstellung) in der .NET Framework.](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp) Auf Ihrem Computer muss Microsoft-Internetinformationsdienste (IIS) installiert sein, um dieses Beispiel ausführen zu können.

## <a name="overview"></a>Übersicht

Bei der No-Touch-Bereitstellung verwenden Tablet PCWindows Forms-Anwendungen Desktopanwendungen, die mithilfe der Klassen im System erstellt wurden. Windows. Der Formularnamespace von Microsoft .NET Framework und microsoft Windows XP Tablet PC Edition Development Kit 1.7 kann heruntergeladen, installiert und direkt auf den Computern der Benutzer ausgeführt werden, ohne dass die Registrierung oder freigegebenen Systemkomponenten geändert werden.

In diesem Beispiel wird das ursprüngliche Projekt für [Auto Claims Form Sample](auto-claims-form-sample.md), AutoClaims und das Installationsprojekt AutoClaims \_ NoTouchWeb verwendet. Nach der Kompilierung und Ausführung erstellt das Installationsprogrammprojekt einen neuen virtuellen Stamm, auch als AutoClaims \_ NoTouchWeb bezeichnet. Das Installationsprogramm kopiert eine Datei default.htm, die einen Link zur AutoClaims.exe enthält. Um die Rich Client-Anwendung zu starten, navigieren Sie zum virtuellen Stamm mit Microsoft Internet Explorer, und klicken Sie dann auf den Link auf der default.htm Seite.

> [!Note]  
> Sie müssen über IIS zum virtuellen Stamm navigieren (z. B. und nicht direkt über das Dateisystem), damit die Anwendung in der Internet Explorer https://localhost/AutoClaims\_NoTouchWeb/default.htm) funktioniert.

 


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



## <a name="no-touch-deployment-requirements"></a>No-Touch Bereitstellungsanforderungen

Alle abhängigen Assemblys müssen sich entweder im Assemblysuchpfad oder im Stammverzeichnis des virtuellen Verzeichnisses der Website befinden. Das Bereitstellungsprojekt AutoClaims NoTouchWeb installiert die Assembly und die verweisende Seite default.htm im gleichen virtuellen Stamm \_ (AutoClaims \_ NoTouchWeb).

> [!Note]  
> Die kompilierten Webbeispiele werden nicht von der Standardinstallationsoption für das SDK installiert. Sie müssen eine benutzerdefinierte Installation abschließen und die Unteroption "Vor kompilierte Webbeispiele" auswählen, um sie zu installieren.

 

Weitere Informationen zur Verwendung von Ink im Web finden Sie unter [Ink on the Web (Ink im Web).](ink-on-the-web.md)

 

 