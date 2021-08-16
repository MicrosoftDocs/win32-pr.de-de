---
description: Der letzte Schritt besteht darin, einen Verweis auf die Setup.exe auf der hypothetischen MySetup-Webseite (MySetup.html) zu platzieren, die unter Beispiel zur Installation eines URL-basierten Windows Installers beschrieben wird.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Einrichten eines HTML-Verweises auf Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22be693c4e2e411fa724a70f90da4af4af4cf17ad6bb316bd3a483dd55bfd5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378070"
---
# <a name="establish-an-html-reference-to-setupexe"></a>Einrichten eines HTML-Verweises auf Setup.exe

Der letzte Schritt besteht darin, einen Verweis auf die Setup.exe auf der hypothetischen MySetup-Webseite (MySetup.html) zu platzieren, die unter [Beispiel zur Installation eines URL-basierten Windows Installers](a-url-based-windows-installer-installation-example.md)beschrieben wird. Verwenden Sie das folgende HTML-Skript:

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Wenn Sie auf den Link "MySetup-Installation" klicken, haben Benutzer die Möglichkeit, an diesem Speicherort zu speichern oder auszuführen. Wenn der Benutzer von diesem Speicherort ausführen auswählt, aktualisiert der Setup.exe die Version von Windows Installer auf dem Computer, überprüft bei Bedarf die digitale Signatur im Installationspaket und installiert das Paket auf dem Computer.

Damit wird das Beispiel abgeschlossen.

 

 



