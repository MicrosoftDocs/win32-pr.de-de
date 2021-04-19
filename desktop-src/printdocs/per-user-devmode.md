---
description: Ein Benutzer kann die Standarddokument Einstellungen für einen Drucker angeben. Dies wird als benutzerdefinierter DEVMODE bezeichnet, da er nur die Standardwerte für einen bestimmten Benutzer beeinflusst und die Informationen für die einzelnen Drucker in einer separaten DEVMODE-Struktur definiert sind.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee5a79d314e0f9ab89210ba4d2644d2b8ec99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363457"
---
# <a name="per-user-devmode"></a>Per-User DEVMODE

Ein Benutzer kann die Standarddokument Einstellungen für einen Drucker angeben. Dies wird als *benutzerdefinierter DEVMODE* bezeichnet, da er nur die Standardwerte für einen bestimmten Benutzer beeinflusst und die Informationen für die einzelnen Drucker in einer separaten [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Struktur definiert sind.

Um den DEVMODE-Benutzer pro Benutzer festzulegen, nennen Sie [**SetPrinter**](setprinter.md) entweder mit der [**Drucker \_ Info \_ 2**](printer-info-2.md) oder mit der [**Drucker \_ Info \_ 9**](printer-info-9.md) -Struktur. Um den DEVMODE-Benutzer pro Benutzer auf den globalen standardmäßigen [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)zurückzusetzen, nennen Sie **SetPrinter** mit der [**Drucker \_ Info \_ 8**](printer-info-8.md) -Struktur.

 

 



