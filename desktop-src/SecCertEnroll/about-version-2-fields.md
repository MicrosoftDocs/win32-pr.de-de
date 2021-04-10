---
description: Ein X.509-Zertifikat der Version 2 enthält die grundlegenden Felder, die in Version 1 definiert sind, sowie zusätzlich die folgenden Felder.
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: Felder der Version 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e66d66d9c5d92f7c3a0436ae828b60d285edce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214373"
---
# <a name="version-2-fields"></a>Felder der Version 2

Ein X.509-Zertifikat der Version 2 enthält die grundlegenden Felder, die in Version 1 definiert sind, sowie zusätzlich die folgenden Felder.

## <a name="issuer-unique-identifier"></a>Issuer Unique Identifier

Enthält einen eindeutigen Wert, mit dem der X.500-Name der Zertifizierungsstelle eindeutig festgelegt werden kann, wenn dieser im Lauf der Zeit von verschiedenen Entitäten wiederverwendet wird.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a>Issuer Unique Identifier

Enthält einen eindeutigen Wert, mit dem der X.500-Name des Zertifikatantragstellers eindeutig festgelegt werden kann, wenn dieser im Lauf der Zeit von verschiedenen Entitäten wiederverwendet wird.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Felder](about-basic-fields.md)
</dt> <dt>

[Erweiterungen der Version 3](about-version-3-extensions.md)
</dt> <dt>

[X. 509-Zertifikate für öffentliche Schlüssel](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



