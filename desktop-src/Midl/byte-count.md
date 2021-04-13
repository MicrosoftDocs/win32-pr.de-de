---
title: byte_count-Attribut
description: Das Attribut \ Byte \_ count \ ACF ist ein Parameter Attribut, das eine Größe (in Bytes) mit dem durch den Zeiger gekennzeichneten Speicherbereich verknüpft.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count Attribut-Mittel l
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312851"
---
# <a name="byte_count-attribute"></a>Byte \_ Anzahl Attribut

Das ACF-Attribut **\[ Byte \_ Count \]** ist ein Parameter Attribut, das eine Größe (in Bytes) mit dem durch den Zeiger gekennzeichneten Speicherbereich verknüpft.

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Function-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr ACF-Funktions Attribute an.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, die in der IDL-Datei definiert ist. Der Funktionsname ist erforderlich.

</dd> <dt>

*Length-Variable-Name* 
</dt> <dd>

Gibt den Namen des [**\[ \] reinen Parameters an,**](in.md)der die Größe (in Bytes) des Speicherbereichs angibt, auf den durch *Parameter Name* verwiesen wird.

</dd> <dt>

*Parameter Name* 
</dt> <dd>

Gibt den Namen des reinen Zeiger Parameters an [**\[ , \]**](out-idl.md)der in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\[ Byte \_ Anzahl \]** der ACF-Attribute stellt eine Microsoft-Erweiterung für DCE-IDL dar. Daher ist dieses Attribut nicht verfügbar, wenn Sie den Mittelwert-Compilerschalter [**/OSF**](-osf.md)verwenden.

> [!Note]  
> Das **\[ Byte Count \]** -Attribut wird in der NDR64-Syntax nicht mehr unterstützt, da die für alle [**\[ out \]**](out-idl.md) -Parameter erforderliche Größe nicht zu schätzen ist.

 

Der Arbeitsspeicher, auf den der Zeiger Parameter verweist, ist zusammenhängend und wird nicht von den Client-stubden zugewiesen oder freigegeben. Mit dieser Funktion des **\[ Byte \_ Count \]** -Attributs können Sie einen persistenten Pufferbereich im Client Speicher erstellen, der bei mehr als einem Remote Prozedur Abruf wieder verwendet werden kann.

Durch die Möglichkeit, die Speicher Belegung für den Client-Stub zu deaktivieren, können Sie die Anwendung auf Effizienz optimieren. Beispielsweise kann das **\[ Byte \_ Count \]** -Attribut von Dienstanbieter Funktionen verwendet werden, die Microsoft RPC verwenden. Wenn eine Benutzeranwendung die Dienstanbieter-API aufruft und einen Zeiger an einen Puffer sendet, kann der Dienstanbieter den Puffer Zeiger an die Remote Funktion übergeben. Der Dienstanbieter kann den Puffer bei mehreren Remote aufrufen wieder verwenden, ohne den Benutzer zu zwingen, den Speicherbereich neu zuzuordnen.

Der Arbeitsspeicher Bereich kann komplexe Datenstrukturen enthalten, die aus mehreren Zeigern bestehen. Da der Speicherbereich zusammenhängend ist, muss die Anwendung nicht mehrere Aufrufe durchführen, um jeden Zeiger und jede Struktur einzeln freizugeben. Stattdessen kann der Speicherbereich mit einem Rückruf der Speicher Belegung oder der kostenlosen Routine zugeordnet oder freigegeben werden.

Bei dem Puffer muss es sich um einen reinen [**\[ out \]**](out-idl.md)-Parameter handeln, während die Pufferlänge in [**\[ \] Byte einen reinen**](in.md)Parameter aufweisen muss.

Geben Sie einen Puffer an, der groß genug ist, um alle [**\[ out \]**](out-idl.md) -Parameter zu enthalten. Verwenden Sie wegen ausgeblendeter Auffüll Zeichen anstelle von exakten Anzahlen eine Überschätzung. Beispielsweise werden 4-Byte-Zeiger auf eine 4-Byte-Ausrichtung auf 32-Bit-Plattformen und 8-Byte-Zeiger auf eine 8-Byte-Grenze auf 64-Bit-Plattformen gemarshallt. Daher muss die Ausrichtungs Auffüllung, die die stubvorgänge ausführen, im Speicherplatz für den Puffer berücksichtigt werden. Außerdem können die während der Kompilierung der C-Sprache verwendeten Verpackungs Ebenen variieren. Verwenden Sie einen Byte Zählerwert, der zusätzliche Komprimierungs Bytes für den während der Kompilierung in der C-Sprache verwendeten Verpackungs Grad berücksichtigt. Ein sicheres Verfahren, das sowohl 32-Bit-als auch 64-Bit-Plattformen abdeckt, besteht darin, dass jedes Objekt, das in den großen Speicherblock geht, an einer Adresse beginnt, die ein Vielfaches von 8 ist.

## <a name="examples"></a>Beispiele

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**Länge \_ ist**](length-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**Größe \_ :**](size-is.md)
</dt> </dl>

 

 




