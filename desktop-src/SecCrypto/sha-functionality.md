---
description: Der ursprüngliche Basis Anbieter hat fälschlicherweise gemeldet, dass der SHA-Hash Algorithmus Algorithmen durch Aufrufe von "CryptGetProvParam" mit dem angegebenen Parameter "PP \_ enumalgs" auflistet.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: SHA-Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749560"
---
# <a name="sha-functionality"></a>SHA-Funktionalität

Der ursprüngliche Basis Anbieter hat fälschlicherweise gemeldet, dass der [*SHA*](../secgloss/s-gly.md) -Hash Algorithmus Algorithmen durch Aufrufe von " [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) " mit dem angegebenen Parameter "PP \_ enumalgs" auflistet. Dies wurde im Basis Anbieter behoben. Der überarbeitete Basis Anbieter und der erweiterte Anbieter melden nun SHA-1 ordnungsgemäß.

Eine definierte calg \_ SHA1-Konstante wurde Wincrypt. h mit dem gleichen Wert wie calg SHA hinzugefügt \_ .

 

 
