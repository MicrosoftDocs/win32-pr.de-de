---
description: Ein Benutzer kann die Standarddokumenteinstellungen für einen Drucker angeben. Dies wird als devMODE pro Benutzer bezeichnet, da es sich nur auf die Standardwerte für einen bestimmten Benutzer be auswirken und die Informationen für jeden Drucker in einer separaten DEVMODE-Struktur definiert sind.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5e9fd2872d055dba6d04f060e6d2e581e461fd20ddc418f643d09170cda31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731925"
---
# <a name="per-user-devmode"></a>Per-User DEVMODE

Ein Benutzer kann die Standarddokumenteinstellungen für einen Drucker angeben. Dies wird als *devMODE pro* Benutzer bezeichnet, da es sich nur auf die Standardwerte für einen bestimmten Benutzer be auswirken und die Informationen für jeden Drucker in einer separaten [**DEVMODE-Struktur definiert**](/windows/win32/api/wingdi/ns-wingdi-devmodea) sind.

Rufen Sie [**setPrinter**](setprinter.md) mit der PRINTER INFO [**\_ \_ 2-**](printer-info-2.md) oder [**PRINTER \_ INFO \_ 9-Struktur**](printer-info-9.md) auf, um den pro Benutzer festgelegten DEVMODE-Wert zu verwenden. Rufen Sie **SetPrinter** mit der [**PRINTER INFO \_ \_ 8-Struktur**](printer-info-8.md) auf, um den PRO-Benutzer-DEVMODE auf den globalen [**Standard-DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)zurückzusetzen.

 

 



