---
description: '\_Gebiets Schema slongdate'
ms.assetid: 1b72cd57-819e-4b1f-bbb0-b600a9e8631c
title: LOCALE_SLONGDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503b24d81318f471b33a4ab644a059607e5ac490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129685"
---
# <a name="locale_slongdate"></a>\_Gebiets Schema slongdate

Lange Datums Formatierungs Zeichenfolge für das Gebiets Schema. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig ist, ist 80, einschließlich eines abschließenden NULL-Zeichens. Die Zeichenfolge kann aus einer Kombination von [Format Bildern für Tag, Monat, Jahr und ERA](day--month--year--and-era-format-pictures.md) bestehen und jede Zeichenfolge, die in einfache Anführungszeichen eingeschlossen ist. Zeichen in einfachen Anführungszeichen bleiben wie angegeben. Das lange Datum für Spanisch (Spanien) lautet beispielsweise "dddd, dd ' de ' MMMM ' de ' yyyy". Gebiets Schemas können mehrere lange Datumsformate definieren.

Um alle langen Datumsformate für ein Gebiets Schema zu erhalten, verwenden Sie [enumdateformats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [enumdateformatsex](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)oder [enumdateformatsexex](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).

 

 



