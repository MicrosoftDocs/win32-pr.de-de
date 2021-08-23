---
description: Um eine öffentliche Eigenschaft auf einen Literalzeichenfolgenwert festzulegen, schließen Sie die Zeichenfolge zwischen Anführungszeichen ein.
ms.assetid: ec2626fa-a3be-45e5-a566-658206d3d0bb
title: Festlegen öffentlicher Eigenschaftswerte in der Befehlszeile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db6c2f2b46a50ced914112b0ecb2b889c130ee7044130c11def9ad4ea0a5c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624935"
---
# <a name="setting-public-property-values-on-the-command-line"></a>Festlegen öffentlicher Eigenschaftswerte in der Befehlszeile

Um eine öffentliche Eigenschaft auf einen Literalzeichenfolgenwert festzulegen, schließen Sie die Zeichenfolge zwischen Anführungszeichen ein.

PROPERTY = "string"

Die Anführungszeichen sind nur erforderlich, wenn die Zeichenfolge Leerzeichen enthält. Um eine öffentliche Eigenschaft in einer Befehlszeile zu löschen (legen Sie sie auf NULL fest), legen Sie den Wert der Eigenschaft auf eine leere Zeichenfolge fest. In diesem Fall sind Anführungszeichen erforderlich.

PROPERTY="".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> <dt>

[Abrufen und Festlegen von Eigenschaften](getting-and-setting-properties.md)
</dt> </dl>

 

 



