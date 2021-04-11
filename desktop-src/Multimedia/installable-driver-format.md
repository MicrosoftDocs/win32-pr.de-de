---
title: Installier bares Treiber Format
description: Installier bares Treiber Format
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- installierbare Treiber, Formate
- installierbare Treiber, driverproc-Funktion
- installierbare Treiber, Meldungen
- Treiber Meldungen
- Treiber Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314955"
---
# <a name="installable-driver-format"></a>Installier bares Treiber Format

Jeder installierbare Treiber exportiert eine [driverproc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) -Funktion. Diese allgemeine Einstiegspunkt Funktion empfängt *Treiber Nachrichten* vom System, die den Treiber dazu leiten, Aktionen auszuführen oder Informationen bereitzustellen. Das System sendet Treiber Nachrichten an die Funktion " **driverproc** ", wenn eine Anwendung oder dll den Treiber öffnet oder schließt oder wenn Sie anfordert, dass eine Nachricht an den Treiber gesendet wird. Die **driverproc** -Funktion verarbeitet entweder die Nachricht oder übergibt die Nachricht an den Standard Nachrichten Handler, die [defdriverproc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) -Funktion. In beiden Fällen muss von **driverproc** ein Wert zurückgegeben werden, der angibt, ob die angeforderte Aktion erfolgreich war.

 

 