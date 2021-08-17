---
description: In diesem Beispiel wird gezeigt, wie Sie eine verwaltete Tablet PC-Anwendung über das Web mithilfe der Bereitstellung ohne Toucheingabe bereitstellen.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: Webbeispiel für No-Touch-Bereitstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d8fb9989785dc081022c2e76d8fade6d48bf521b3f27449ff5aac963706f356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449651"
---
# <a name="no-touch-deployment-web-sample"></a>Webbeispiel für No-Touch-Bereitstellung

In diesem Beispiel wird gezeigt, wie Sie eine verwaltete Tablet PC-Anwendung über das Web mithilfe der Bereitstellung ohne Toucheingabe bereitstellen. Sie sollten mit den Konzepten vertraut sein, die unter [No-Touch-Bereitstellung im .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp)erläutert werden. Auf Ihrem Computer muss Microsoft-Internetinformationsdienste (IIS) installiert sein, um dieses Beispiel ausführen zu können.

## <a name="overview"></a>Übersicht

Bei der Bereitstellung ohne Toucheingabe werden Tablet PCWindows Forms-Anwendungen und Desktopanwendungen erstellt, die mithilfe der Klassen im System erstellt wurden. Windows. Der Forms-Namespace der Microsoft .NET Framework und des Microsoft Windows XP Tablet PC Edition Development Kit 1.7 kann heruntergeladen, installiert und direkt auf den Computern der Benutzer ausgeführt werden, ohne änderungen an der Registrierung oder den freigegebenen Systemkomponenten vornehmen zu müssen.

Dieses Beispiel verwendet das ursprüngliche Projekt für [Auto Claims Form Sample](auto-claims-form-sample.md), AutoClaims und stellt das Installationsprogrammprojekt AutoClaims \_ NoTouchWeb bereit. Nach der Kompilierung und Ausführung erstellt das Installationsprogrammprojekt einen neuen virtuellen Stamm, der auch AutoClaims \_ NoTouchWeb genannt wird. Das Installationsprogramm kopiert eine Datei default.htm, die einen Link zur AutoClaims.exe Assembly enthält. Navigieren Sie zum Starten der Rich Client-Anwendung zum virtuellen Stamm mit Microsoft Internet Explorer, und klicken Sie dann auf der Seite default.htm auf den Link.

> [!Note]  
> Sie müssen über IIS zum virtuellen Stamm navigieren (z. B. https://localhost/AutoClaims\_NoTouchWeb/default.htm) und nicht direkt über das Dateisystem, damit die Anwendung in der Anwendungsdomäne Internet Explorer funktioniert.

 


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

Alle abhängigen Assemblys müssen sich entweder im Assemblysuchpfad oder im Stammverzeichnis des virtuellen Verzeichnisses der Website befinden. Das Bereitstellungsprojekt AutoClaims \_ NoTouchWeb installiert die Assembly und die verweisende Seite default.htm im gleichen virtuellen Stammverzeichnis (AutoClaims \_ NoTouchWeb).

> [!Note]  
> Die kompilierten Webbeispiele werden nicht von der Standardinstallationsoption für das SDK installiert. Sie müssen eine benutzerdefinierte Installation abschließen und die Unteroption "Vorkompilierte Webbeispiele" auswählen, um sie zu installieren.

 

Weitere Informationen zur Verwendung von Ink im Web finden Sie unter [Ink im Web.](ink-on-the-web.md)

 

 