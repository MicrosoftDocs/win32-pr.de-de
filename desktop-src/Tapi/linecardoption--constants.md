---
description: Die linecardoption- \_ Konstanten definieren Werte, die im dwOptions-Member der linecardentry-Struktur verwendet werden, die als Teil der linetranslatecaps-Struktur zurückgegeben wird, die von linegettranslatecaps zurückgegeben wurde.
ms.assetid: 36c67fbf-e5ca-4ec4-a03a-0b828667abcc
title: LINECARDOPTION_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9948d4a8963e8a9c860f68f0067c601f602c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370857"
---
# <a name="linecardoption_-constants"></a>Linecardoption- \_ Konstanten

Die **linecardoption \_ -Konstanten** definieren Werte, die im **dwOptions** -Member der [**linecardentry**](/windows/desktop/api/Tapi/ns-tapi-linecardentry) -Struktur verwendet werden, die als Teil der [**linetranslatecaps**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) -Struktur zurückgegeben wird, die von [**linegettranslatecaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)zurückgegeben wurde. Die **linecardoption- \_ Konstanten** t weisen die folgenden Werte auf:

<dl> <dt>

<span id="LINECARDOPTION_HIDDEN"></span><span id="linecardoption_hidden"></span>**linecardoption \_ ausgeblendet**
</dt> <dd> <dl> <dt>



Diese Aufruf Karte wurde vom Benutzer ausgeblendet. Sie wird in der Haupt Auflistung der verfügbaren Aufruf Karten nicht durch das Dial-Hilfsobjekt angezeigt, wird jedoch in der Liste der Karten angezeigt, von denen die Regeln zum abwählen kopiert werden können.


</dt> </dl> </dd> <dt>

<span id="LINECARDOPTION_PREDEFINED"></span><span id="linecardoption_predefined"></span>**linecardoption \_ vordefiniert**
</dt> <dd> <dl> <dt>



Diese Aufruf Karte ist eine der vordefinierten Aufruf Karten Definitionen, die von Microsoft in der Telefoniekarte enthalten sind. Sie kann nicht vollständig mithilfe von Dial Helper entfernt werden. Wenn der Benutzer versucht, ihn zu entfernen, wird er ausgeblendet. Auf diese Weise ist der Zugriff auf das Kopieren von Wähl Regeln weiterhin möglich.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Nicht erweiterbar. Alle 32 Bits sind reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




