---
description: Geschützte Daten werden als ASN. 1-codiertes BLOB gespeichert.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Geschütztes Daten Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131300"
---
# <a name="protected-data-format"></a>Geschütztes Daten Format

Geschützte Daten werden als ASN. 1-codiertes BLOB gespeichert. Die Daten werden als CMS-Inhalte (Certificate Message Syntax) formatiert. Der digitale Umschlag enthält verschlüsselte Inhalte, Empfängerinformationen, die einen verschlüsselten Inhalts Verschlüsselungsschlüssel (CEK) enthalten, und einen Header, der Informationen über den Inhalt enthält, einschließlich der unverschlüsselten Schutz Deskriptor-Regel Zeichenfolge. Dies wird im folgenden Diagramm dargestellt.

![geschützte eingehüllte Daten](images/protecteddatablob.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CNG-DPAPI](cng-dpapi.md)
</dt> <dt>

[Schutz Deskriptoren](protection-descriptors.md)
</dt> <dt>

[Schutz Anbieter](protection-providers.md)
</dt> </dl>

 

 



