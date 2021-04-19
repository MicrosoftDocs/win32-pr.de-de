---
description: Bevor eine Anwendung Daten zur Registrierung hinzufügen kann, muss Sie einen Schlüssel erstellen oder öffnen.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Öffnen, erstellen und Schließen von Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3260c255240ce2c7fb5d13fe28126a1a3f5527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353126"
---
# <a name="opening-creating-and-closing-keys"></a>Öffnen, erstellen und Schließen von Schlüsseln

Bevor eine Anwendung Daten zur Registrierung hinzufügen kann, muss Sie einen Schlüssel erstellen oder öffnen. Um einen Schlüssel zu erstellen oder zu öffnen, verweist eine Anwendung immer auf den Schlüssel als Unterschlüssel eines aktuell geöffneten Schlüssels. Die folgenden vordefinierten Schlüssel sind immer geöffnet: **HKEY \_ local \_ Machine**, **HKEY \_ Classes \_ root**, **HKEY \_ Users** und **HKEY \_ Current \_ User**. Eine Anwendung verwendet die [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) -Funktion, um einen Schlüssel zu öffnen, und die [**regkreatekeyex**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) -Funktion, um einen Schlüssel zu erstellen. Eine Registrierungs Struktur kann 512 Ebenen tief sein. Sie können bis zu 32 Ebenen gleichzeitig über einen einzigen Registrierungs-API-Aufruf erstellen.

Eine Anwendung kann die [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) -Funktion verwenden, um einen Schlüssel zu schließen und die darin enthaltenen Daten in die Registrierung zu schreiben. **RegCloseKey** schreibt die Daten vor der Rückgabe nicht notwendigerweise in die Registrierung. Es kann bis zu mehrere Sekunden dauern, bis der Cache auf die Festplatte geleert wird. Wenn eine Anwendung explizit Registrierungsdaten auf die Festplatte schreiben muss, kann Sie die [**regflushkey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) -Funktion verwenden. **Regflushkey** verwendet jedoch viele Systemressourcen und sollte nur aufgerufen werden, wenn dies unbedingt erforderlich ist.

 

 



