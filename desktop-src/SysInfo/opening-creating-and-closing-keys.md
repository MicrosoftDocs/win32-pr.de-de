---
description: Bevor eine Anwendung Daten zur Registrierung hinzufügen kann, muss sie einen Schlüssel erstellen oder öffnen.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Öffnen, Erstellen und Schließen von Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605d53a00506122c6350abd7f06e9166ed487de98c7910a3b7c3a913978492f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763962"
---
# <a name="opening-creating-and-closing-keys"></a>Öffnen, Erstellen und Schließen von Schlüsseln

Bevor eine Anwendung Daten zur Registrierung hinzufügen kann, muss sie einen Schlüssel erstellen oder öffnen. Um einen Schlüssel zu erstellen oder zu öffnen, verweist eine Anwendung immer auf den Schlüssel als Unterschlüssel eines derzeit geöffneten Schlüssels. Die folgenden vordefinierten Schlüssel sind immer geöffnet: **HKEY \_ LOCAL \_ MACHINE**, **HKEY \_ CLASSES \_ ROOT**, **HKEY \_ USERS** und **HKEY CURRENT \_ \_ USER**. Eine Anwendung verwendet die [**RegOpenKeyEx-Funktion,**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) um einen Schlüssel zu öffnen, und die [**RegCreateKeyEx-Funktion,**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) um einen Schlüssel zu erstellen. Eine Registrierungsstruktur kann 512 Ebenen tief sein. Sie können bis zu 32 Ebenen gleichzeitig über einen einzelnen Registrierungs-API-Aufruf erstellen.

Eine Anwendung kann die [**RegCloseKey-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) verwenden, um einen Schlüssel zu schließen und die darin enthaltenen Daten in die Registrierung zu schreiben. **RegCloseKey** schreibt die Daten nicht unbedingt vor der Rückgabe in die Registrierung. Es kann bis zu mehrere Sekunden dauern, bis der Cache auf die Festplatte geleert wird. Wenn eine Anwendung explizit Registrierungsdaten auf die Festplatte schreiben muss, kann sie die [**RegFlushKey-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) verwenden. **RegFlushKey** verwendet jedoch viele Systemressourcen und sollte nur aufgerufen werden, wenn dies unbedingt erforderlich ist.

 

 



