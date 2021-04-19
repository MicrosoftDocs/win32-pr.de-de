---
description: Elliptische Kurven in den Windows 10-Versionen 1507 und 1511.
title: Elliptische TLS-Kurven in Windows 10, Version 1507 und 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: c38d1014433e1274d8dff52be09d59761d3b1761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359446"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a>Elliptische TLS-Kurven in Windows 10, Version 1507 und 1511

Für Windows 10, Version 1507 und 1511, sind die folgenden elliptischen Kurven aktiviert, und in dieser Prioritäts Reihenfolge wird standardmäßig der Microsoft SChannel-Anbieter verwendet:

| Zeichenfolge mit elliptischer Kurve | Verfügbar im PPS-Modus |
|-------------|--------------|
| Benannte nistp256 | Ja |
| Benannte nistp384 | Ja |


Die folgenden elliptischen Kurven werden vom Microsoft SChannel-Anbieter unterstützt, sind jedoch nicht standardmäßig aktiviert:

| Zeichenfolge mit elliptischer Kurve | Verfügbar im PPS-Modus |
|-------------|--------------|
| benannte brainpoolp256r1 | Nein |
| benannte brainpoolp384r1 | Nein |
| benannte brainpoolp512r1 | Nein |
| nistP192 | Nein |
| nistP224 | Nein |
| benannte nistp521 | Ja |
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

## <a name="enabling-elliptic-curves"></a>Aktivieren von elliptischen Kurven

Um elliptische Kurven hinzuzufügen, stellen Sie entweder eine Gruppenrichtlinie bereit, oder verwenden Sie die TLS-Cmdlets:
- Um die Gruppenrichtlinie zu verwenden, konfigurieren Sie die [ECC-Kurven Reihenfolge](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) unter Computer Konfiguration > administrative Vorlagen > Netzwerk > SSL-Konfigurationseinstellungen mit der Prioritäts Liste für alle elliptischen Kurven, die Sie aktivieren möchten.

- Informationen zur Verwendung von PowerShell finden Sie unter [TLS-Cmdlets](/powershell/module/tls) für eine komplette Liste der TLS-Cmdlet-Syntax und Beschreibungen.


> [!NOTE]
> Vor Windows 10 wurden Chiffre Sammlungs Zeichenfolgen mit der elliptischen Kurve angehängt, um die Kurven Priorität zu bestimmen. Windows 10 unterstützt eine Einstellung für die Prioritäts Reihenfolge der elliptischen Kurven, damit das elliptische Kurven Suffix nicht erforderlich ist und von der neuen Priorität der elliptischen Kurven Priorität außer Kraft gesetzt wird, um Organisationen die Verwendung von Gruppenrichtlinien zum Konfigurieren verschiedener Versionen von Windows mit denselben Verschlüsselungs Sammlungen zu ermöglichen.


## <a name="see-also"></a>Weitere Informationen

[Konfigurieren der TLS ECC-Kurven Reihenfolge](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Verwalten der TLS ECC-Reihenfolge](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[Verwalten von Windows ECC-Kurven mithilfe von Gruppenrichtlinie](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[TLS-Cmdlets](/powershell/module/tls)
