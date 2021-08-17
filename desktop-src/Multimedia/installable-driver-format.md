---
title: Installierbares Treiberformat
description: Installierbares Treiberformat
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- Installierbare Treiber, Formate
- Installierbare Treiber, DriverProc-Funktion
- Installierbare Treiber, Meldungen
- Treibermeldungen
- Treiberformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c02f6bb2515d1f182146b84b7f0b971fa4b73fe2e2caf5abf63dfd4ddb272df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140789"
---
# <a name="installable-driver-format"></a>Installierbares Treiberformat

Jeder installierbare Treiber exportiert eine [DriverProc-Funktion.](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) Diese allgemeine Einstiegspunktfunktion empfängt *Treibermeldungen vom* System, die den Treiber an die Durchführung von Aktionen oder die Bereitstellung von Informationen verweisen. Das System sendet Treibermeldungen an die **DriverProc-Funktion,** wenn eine Anwendung oder DLL den Treiber öffnet oder schließt oder eine Nachricht an den Treiber sendet. Die **DriverProc-Funktion** verarbeitet entweder die Nachricht oder übergibt die Nachricht an den Standardnachrichtenhandler, die [DefDriverProc-Funktion.](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) In beiden Fällen muss **DriverProc** einen Wert zurückgeben, der angibt, ob die angeforderte Aktion erfolgreich war.

 

 