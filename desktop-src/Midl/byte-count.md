---
title: byte_count-Attribut
description: Das Attribut \byte count\ ACF ist ein Parameterattribut, das eine Größe in Bytes dem durch den Zeiger angegebenen \_ Arbeitsspeicherbereich zugibt.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count MIDL-Attribut
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffd42e27be4768fc0817aa76bb366429e236b3a82c45d081a05485b8520a23a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807823"
---
# <a name="byte_count-attribute"></a>\_Byteanzahlattribut

Das **\[ Byteanzahl-ACF-Attribut \_ \]** ist ein Parameterattribut, das eine Größe in Bytes dem durch den Zeiger angegebenen Arbeitsspeicherbereich zugibt.

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*function-attribute-list* 
</dt> <dd>

Gibt null oder mehr ACF-Funktionsattribute an.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, die in der IDL-Datei definiert ist. Der Funktionsname ist erforderlich.

</dd> <dt>

*length-variable-name* 
</dt> <dd>

Gibt den Namen des [**\[ parameters \] in**](in.md)-only an, der die Größe des Arbeitsspeicherbereichs in Bytes angibt, auf den der *Parametername verweist.*

</dd> <dt>

*Parametername* 
</dt> <dd>

Gibt den Namen des out-only-Zeigerparameters [**\[ \]**](out-idl.md)an, der in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\[ Byteanzahl des \_ ACF-Attributs \]** stellt eine Microsoft-Erweiterung für DCE-IDL dar. Daher ist dieses Attribut nicht verfügbar, wenn Sie den MIDL-Compilerschalter [**/osf verwenden.**](-osf.md)

> [!Note]  
> Das **\[ Byteanzahlattribut \]** wird in der NDR64-Syntax aufgrund der Schwierigkeiten bei der Schätzung der erforderlichen Größe für alle out-Parameter [**\[ nicht mehr \]**](out-idl.md) unterstützt.

 

Der Arbeitsspeicher, auf den der Zeigerparameter verweist, ist zusammenhängend und wird von den Clientstubs nicht zugeordnet oder frei. Mit diesem Feature des **\[ \_ \] Byteanzahlattributs** können Sie einen persistenten Pufferbereich im Clientspeicher erstellen, der bei mehr als einem Aufruf der Remoteprozedur wiederverwendet werden kann.

Durch die Möglichkeit, die Speicherzuweisung des Clientstubs zu deaktivieren, können Sie die Anwendung auf Effizienz optimieren. Beispielsweise kann das **\[ \_ Byteanzahlattribut \]** von Dienstanbieterfunktionen verwendet werden, die Microsoft RPC verwenden. Wenn eine Benutzeranwendung die Dienstanbieter-API aufruft und einen Zeiger auf einen Puffer sendet, kann der Dienstanbieter den Pufferzeiger an die Remotefunktion übergeben. Der Dienstanbieter kann den Puffer bei mehreren Remoteaufrufen wiederverwenden, ohne dass der Benutzer gezwungen wird, den Arbeitsspeicherbereich neu zu verwenden.

Der Speicherbereich kann komplexe Datenstrukturen enthalten, die aus mehreren Zeigern bestehen. Da der Speicherbereich zusammenhängend ist, muss die Anwendung nicht mehrere Aufrufe zur individuellen Freistellung jedes Zeigers und jeder Struktur tätigen. Stattdessen kann der Speicherbereich mit einem Aufruf der Speicherzuweisung oder der freien Routine reserviert oder frei werden.

Der Puffer muss ein [**\[ \]**](out-idl.md)out-only-Parameter sein, während die Pufferlänge in Bytes ein [**\[ in \]**](in.md)-only-Parameter sein muss.

Geben Sie einen Puffer an, der groß genug ist, um alle [**\[ out-Parameter zu \]**](out-idl.md) enthalten. Verwenden Sie aufgrund der ausgeblendeten Auf padding Überschätzungen anstelle der genauen Anzahl. Beispielsweise werden 4-Byte-Zeiger an einer 4-Byte-ausgerichteten Grenze auf 32-Bit-Plattformen und 8-Byte-Zeigern auf einer 8-Byte-Grenze auf 64-Bit-Plattformen nichtmarshaliert. Daher muss die Ausrichtungsauf padding, die die Stubs ausführen, im Pufferbereich berücksichtigt werden. Darüber hinaus können die während der C-Sprachkompilierung verwendeten Packebenen variieren. Verwenden Sie einen Byteanzahlwert, der zusätzliche Packbytes für die Packebene, die während der C-Sprachkompilierung verwendet wird, eingerechnet. Eine sichere Methode, die sowohl 32-Bit-Plattformen als auch 64-Bit-Plattformen abdeckt, besteht in der Annahme, dass jedes Objekt, das in den großen Speicherblock geht, an einer Adresse beginnt, die ein Vielfaches von 8 ist.

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

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**length \_ ist**](length-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**size \_ ist**](size-is.md)
</dt> </dl>

 

 




