---
description: Geschützte Daten werden als ASN.1-codiertes BLOB gespeichert.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Geschütztes Datenformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b4985fee02b5c40b9ad51a6645c4e0d9894a358a871c2067e44dd5f90da26c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907406"
---
# <a name="protected-data-format"></a>Geschütztes Datenformat

Geschützte Daten werden als ASN.1-codiertes BLOB gespeichert. Die Daten werden als CMS-Inhalt (Certificate Message Syntax) formatiert. Der digitale Umschlag enthält verschlüsselte Inhalte, Empfängerinformationen, die einen verschlüsselten Inhaltsverschlüsselungsschlüssel (Content Encryption Key, CEK) enthalten, und einen Header, der Informationen zum Inhalt enthält, einschließlich der Deskriptorregelzeichenfolge für unverschlüsselten Schutz. Dies wird im folgenden Diagramm veranschaulicht.

![geschützte umschlagete Daten](images/protecteddatablob.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[Schutzdeskriptoren](protection-descriptors.md)
</dt> <dt>

[Schutzanbieter](protection-providers.md)
</dt> </dl>

 

 



