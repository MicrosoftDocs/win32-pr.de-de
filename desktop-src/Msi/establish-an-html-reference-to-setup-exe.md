---
description: Der letzte Schritt ist das Platzieren eines Verweises auf die Setup.exe auf der hypothetischen mySetup-Webseite (MySetup.html), die in einem URL-basierten Windows Installer-Installations Beispiel beschrieben wird.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Erstellen eines HTML-Verweises auf Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216369"
---
# <a name="establish-an-html-reference-to-setupexe"></a>Erstellen eines HTML-Verweises auf Setup.exe

Der letzte Schritt ist das Platzieren eines Verweises auf die Setup.exe auf der hypothetischen mySetup-Webseite (MySetup.html), die in [einem URL-basierten Windows Installer-Installations Beispiel](a-url-based-windows-installer-installation-example.md)beschrieben wird. Verwenden Sie das folgende HTML-Skript:

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Durch Klicken auf den Link "mySetup-Installation" werden Benutzern die Option zum Speichern oder ausführen an diesem Speicherort angezeigt. Wenn der Benutzer die Option Ausführen von diesem Speicherort aus auswählt Setup.exe, wird die-Version der Windows Installer auf dem Computer aktualisiert, falls erforderlich, die digitale Signatur des Installationspakets überprüft und das Paket auf dem Computer installiert.

Dies schließt das Beispiel ab.

 

 



