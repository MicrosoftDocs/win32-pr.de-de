---
description: Elliptische Kurven, die in Windows 10 Versionen 1507 und 1511 aktiviert sind.
title: TLS Elliptic Curves in Windows 10 Version 1507 und 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 91dfc7dac8f45b9c4f2231f6db93e776c75544373199170146f55362f02f2be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915865"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a>TLS Elliptic Curves in Windows 10 Version 1507 und 1511

Für Windows 10 versionen 1507 und 1511 werden die folgenden elliptischen Kurven aktiviert und in dieser Prioritätsreihenfolge standardmäßig mit dem Microsoft Schannel-Anbieter verwendet:

| Elliptische Kurvenzeichenfolge | Verfügbar im FIPS-Modus |
|-------------|--------------|
| NistP256 | Ja |
| NistP384 | Ja |


Die folgenden elliptischen Kurven werden vom Microsoft Schannel-Anbieter unterstützt, sind jedoch nicht standardmäßig aktiviert:

| Elliptische Kurvenzeichenfolge | Verfügbar im FIPS-Modus |
|-------------|--------------|
| brainpoolP256r1 | Nein |
| brainpoolP384r1 | Nein |
| brainpoolP512r1 | Nein |
| nistP192 | Nein |
| nistP224 | Nein |
| nistP521 | Ja |
| secP160k1 | Nein |
| secP160r1 | Nein |
| secP160r2 | Nein |
| secP192k1 | Nein |
| secP192r1 | Nein |
| secP224k1 | Nein |
| secP224r1 | Nein |
| secP256k1 | Nein |
| secP256r1 | Nein |
| secP384r1 | Nein |
| secP521r1 | Nein |

## <a name="enabling-elliptic-curves"></a>Aktivieren elliptischer Kurven

Um elliptische Kurven hinzuzufügen, stellen Sie entweder eine Gruppenrichtlinie bereit, oder verwenden Sie die TLS-Cmdlets:
- Um Gruppenrichtlinien zu verwenden, [konfigurieren Sie ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) unter Computerkonfiguration > Administrative Vorlagen > Network > SSL-Konfiguration Einstellungen mit der Prioritätsliste für alle elliptischen Kurven, die Sie aktivieren möchten.

- Eine vollständige Liste der SYNTAX und Beschreibungen von [TLS-Cmdlets](/powershell/module/tls) finden Sie unter TLS-Cmdlets, um PowerShell zu verwenden.


> [!NOTE]
> Vor Windows 10 wurden Verschlüsselungssammlungszeichenfolgen mit der elliptischen Kurve angefügt, um die Kurvenpriorität zu bestimmen. Windows 10 unterstützt eine Prioritätsreihenfolgeeinstellung für elliptische Kurven, sodass das Suffix der elliptischen Kurve nicht erforderlich ist und durch die neue Prioritätsreihenfolge der elliptischen Kurve überschrieben wird, wenn sie bereitgestellt wird, damit Organisationen gruppenrichtlinien verwenden können, um verschiedene Versionen von Windows mit denselben Verschlüsselungssammlungen zu konfigurieren.


## <a name="see-also"></a>Weitere Informationen

[Konfigurieren der TLS ECC-Kurvenreihenfolge](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Verwalten der TLS ECC-Reihenfolge](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[Verwalten von Windows ECC-Kurven mithilfe von Gruppenrichtlinie](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[TLS-Cmdlets](/powershell/module/tls)
