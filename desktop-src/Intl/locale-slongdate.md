---
description: LOCALE \_ SLONGDATE
ms.assetid: 1b72cd57-819e-4b1f-bbb0-b600a9e8631c
title: LOCALE_SLONGDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e47409d99d4db9afa2e684d3be8ae2f874200d56d748868eaa0fa1953452d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106060"
---
# <a name="locale_slongdate"></a>LOCALE \_ SLONGDATE

Lange Datumsformatierungszeichenfolge für das Gebietsschema. Die maximale Anzahl von Zeichen, die für diese Zeichenfolge zulässig sind, ist 80, einschließlich eines abschließenden NULL-Zeichens. Die Zeichenfolge kann aus einer Kombination aus Bildern im [Tag-, Monats-, Jahres- und Zeitraumformat](day--month--year--and-era-format-pictures.md) und einer beliebigen Zeichenfolge bestehen, die in einfache Anführungszeichen eingeschlossen ist. Zeichen in einfachen Anführungszeichen bleiben wie angegeben. Das lange Datum für Spanisch (Spanien) lautet beispielsweise "dddd, dd" de 'MMMM' de 'yyyy'. Gebietsschemas können mehrere lange Datumsformate definieren.

Um alle langen Datumsformate für ein Gebietsschema abzurufen, verwenden Sie [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)oder [EnumDateFormatsExEx.](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)

 

 



