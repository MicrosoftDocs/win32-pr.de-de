---
description: LOCALE \_ \* RETURN-Konstanten
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: LOCALE_RETURN* Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58714897333f69b058588f9050b9bb52ed29c37d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466027"
---
# <a name="locale_return-constants"></a>LOCALE \_ \* RETURN-Konstanten

In diesem Thema werden die LOCALE \_ \* RETURN-Konstanten definiert, die von NLS verwendet werden.




| Wert | Bedeutung | 
|-------|---------|
| LOCALE_RETURN_GENITIVE_NAMES | <strong>Windows 7 und höher:</strong> Rufen Sie die Genitivenamen von Monaten ab. Dies sind die Namen, die verwendet werden, wenn die Monatsnamen mit anderen Elementen kombiniert werden. In "1997" wird beispielsweise das Äquivalent von Januar mit dem Namen " Crypto " geschrieben, wenn der Monat allein benannt wird. Wenn der Monatsname jedoch in Kombination verwendet wird, z. B. in einem Datum wie dem 5. Januar 2003, wird die genitive Form des Namens verwendet. Für das Beispiel "2003" wird der Name des genitiven Monats als "5 beim 2003" angezeigt. Die Liste der genitiven Monatsnamen beginnt mit Januar und ist durch Semikolons getrennt. Wenn es keinen 13. Monat gibt, verwenden Sie ein Semikolon an dessen Stelle am Ende der Liste.<blockquote>[!Note]<br />Genitive-Monatsnamen sind nicht in allen Sprachen vorhanden.</blockquote><br /><br /> | 
| LOCALE_RETURN_NUMBER | <strong>Windows Me/98, Windows NT 4.0 und höher:</strong> Rufen Sie eine Zahl ab. Diese Konstante <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>bewirkt, dass GetLocaleInfo</strong></a> oder <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> einen Wert als Zahl statt als Zeichenfolge abruft. Der Puffer, der den Wert empfängt, muss mindestens die Länge eines DWORD-Werts haben. Diese Konstante kann mit jeder anderen Konstante kombiniert werden, die einen Namen hat, der mit "LOCALE_I" beginnt. | 




 

 

 




