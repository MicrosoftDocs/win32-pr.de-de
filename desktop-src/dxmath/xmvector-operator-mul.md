---
description: Multiplikationsoperatoren.
ms.assetid: f8397999-9956-4d11-8705-c95b788a9f03
title: Operator *-Operatoren
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 374b8ecefd606a9f17b1ae063aeac51158c9fd93514ba9b48dd72b1f19dd8113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117890"
---
# <a name="operator--operators"></a>\*Operatoroperatoren

Multiplikationsoperatoren

### <a name="overload-list"></a>Überladeliste



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Operator</th>
<th style="text-align: left;">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR::operator * (float,XMVECTOR)</strong></a></td>
<td style="text-align: left;">Multiplizieren Eines Gleitkommawerts mit einer Instanz von <code>XMVECTOR</code> , wodurch das Ergebnis eine neue Instanz von zurückgegeben <code>XMVECTOR</code> wird.<br/> <code>operator *</code>Multipliziert einen Gleitkommawert mit jeder Komponente einer Instanz des <a href="xmvector-data-type.md"><strong>XMVECTOR-Datentyps</strong></a>und gibt eine neue <code>XMVECTOR</code> Instanz zurück, deren Komponenten das Ergebnis enthalten. <br/>
<blockquote>
[!Note]<br />
Dieser Operator ist nur unter C++ verfügbar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR::operator * (XMVECTOR,float)</strong></a></td>
<td style="text-align: left;">Multiplizieren Sie eine Instanz von <code>XMVECTOR</code> mit einem Gleitkommawert, und geben Sie dem Ergebnis eine neue Instanz von <code>XMVECTOR</code> zurück.<br/> <code>operator *</code>Multipliziert jede Komponente einer Instanz des <a href="xmvector-data-type.md"><strong>XMVECTOR-Datentyps</strong></a> mit einem Gleitkommawert und gibt eine neue Instanz zurück, <code>XMVECTOR</code> deren Komponenten das Ergebnis enthalten. <br/>
<blockquote>
[!Note]<br />
Dieser Operator ist nur unter C++ verfügbar.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR::operator * (XMVECTOR,XMVECTOR)</strong></a></td>
<td style="text-align: left;">Multipliziert eine Instanz von <code>XMVECTOR</code> mit einer zweiten Instanz und gibt das Ergebnis in einer dritten Instanz zurück. <br/> <code>operator *</code>Multipliziert jede Komponente einer Instanz des <a href="xmvector-data-type.md"><strong>XMVECTOR-Datentyps</strong></a> mit der entsprechenden Komponente in einer zweiten Instanz von <code>XMVECTOR</code> und gibt eine neue Instanz <code>XMVECTOR</code> zurück, die das Ergebnis enthält. <br/>
<blockquote>
[!Note]<br />
Dieser Operator ist nur unter C++ verfügbar.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XMVECTOR-Operatoren](ovw-xmvector-operators.md)
</dt> <dt>

**Referenz**
</dt> <dt>

[**XMVECTOR-Datentyp**](xmvector-data-type.md)
</dt> </dl>

 

 
