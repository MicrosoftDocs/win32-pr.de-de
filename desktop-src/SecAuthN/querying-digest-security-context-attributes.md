---
description: Die QueryContextAttributes (Digest)-Funktion stellt Informationen über die aktuellen Einstellungen eines Sicherheits Kontexts bereit.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Abfragen von Digest-Sicherheitskontext Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959644"
---
# <a name="querying-digest-security-context-attributes"></a>Abfragen von Digest-Sicherheitskontext Attributen

Die [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) -Funktion stellt Informationen über die aktuellen Einstellungen eines [*Sicherheits Kontexts*](../secgloss/s-gly.md)bereit.

Microsoft Digest unterstützt das Abfragen der folgenden Sicherheitskontext Attribute.



| Attribut                   | BESCHREIBUNG                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Informationen zum secpkg- \_ attr- \_ Schlüssel \_     | Informationen in Bezug auf die verwendeten Signatur-und Verschlüsselungsalgorithmen.                                                                                                                                   |
| Informationen zum secpkg- \_ attr- \_ Paket \_ | Allgemeine Informationen zu Microsoft Digest, z. b. die maximale Tokengröße, die vom [*Sicherheitspaket*](../secgloss/s-gly.md)zugelassen wird. |
| secpkg- \_ attr- \_ Größen         | Die maximal zulässige Größe für Nachrichten bezogene Daten, z. b. Signaturen.                                                                                                                                |



 

 

 
