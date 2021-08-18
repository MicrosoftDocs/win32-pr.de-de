---
description: Die QueryContextAttributes (Digest)-Funktion stellt Informationen zu den aktuellen Einstellungen eines Sicherheitskontexts bereit.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Abfragen von Digestsicherheitskontextattributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24499d5119814edec12f29cf5a39ea027f95c100626be1af1d132c952682599c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919959"
---
# <a name="querying-digest-security-context-attributes"></a>Abfragen von Digestsicherheitskontextattributen

Die [**QueryContextAttributes (Digest)-Funktion**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) stellt Informationen zu den aktuellen Einstellungen eines [*Sicherheitskontexts*](../secgloss/s-gly.md)bereit.

Microsoft Digest unterstützt das Abfragen der folgenden Sicherheitskontextattribute.



| attribute                   | BESCHREIBUNG                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SECPKG \_ ATTR \_ KEY \_ INFO     | Informationen zu den verwendeten Signatur- und Verschlüsselungsalgorithmen.                                                                                                                                   |
| SECPKG \_ \_ ATTR-PAKETINFORMATIONEN \_ | Allgemeine Informationen zu Microsoft Digest, z. B. die maximale Tokengröße, die vom [*Sicherheitspaket*](../secgloss/s-gly.md)zugelassen wird. |
| SECPKG \_ \_ ATTR-GRÖßEN         | Die maximal zulässige Größe für nachrichtenbezogene Daten wie Signaturen.                                                                                                                                |



 

 

 
