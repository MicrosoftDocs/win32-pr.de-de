---
description: In diesem Abschnitt wird ein Satz von Windows-Hilfsfunktionen beschrieben, die mit IPropertyBag-Objekten verwendet werden.
ms.assetid: 4ef85855-7eb6-43ec-bf29-1223eaf1a0cc
title: Eigenschaftenbehälterfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b694c579c76be96b00fa8392344ac59bdc0ce42f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550195"
---
# <a name="property-bag-functions"></a>Eigenschaftenbehälterfunktionen

In diesem Abschnitt wird eine Reihe von Windows-Hilfsfunktionen beschrieben, die mit [**IPropertyBag-Objekten**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) verwendet werden.



| Thema                                                                       | Inhalte                                                                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PSPropertyBag \_ Delete**](/windows/win32/api/propsys/nf-propsys-pspropertybag_delete)                     | Löscht eine Eigenschaft aus einem Eigenschaftenbehälter.<br/>                                                                           |
| [**PSPropertyBag \_ ReadBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbool)                 | Liest den **BOOL-Datenwert** einer Eigenschaft in einem Eigenschaftenbehälter.<br/>                                                    |
| [**PSPropertyBag \_ ReadBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbstr)                 | Liest einen **BSTR-Datenwert** aus einer Eigenschaft in einem Eigenschaftenbehälter.<br/>                                                    |
| [**PSPropertyBag \_ ReadDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readdword)               | Liest einen **DWORD-Datenwert** aus der -Eigenschaft in einem Eigenschaftenbehälter.<br/>                                                     |
| [**PSPropertyBag \_ ReadGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readguid)                 | Liest den GUID-Datenwert aus einer Eigenschaft in einem Eigenschaftenbehälter.<br/>                                                      |
| [**PSPropertyBag \_ ReadInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readint)                   | Liest einen **int-Datenwert** aus einer Eigenschaft in einem Eigenschaftenbehälter.<br/>                                                    |
| [**PSPropertyBag \_ ReadLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readlong)                 | Liest einen **LONG-Datenwert** aus einer Eigenschaft in einem Eigenschaftenbehälter.<br/>                                                    |
| [**PSPropertyBag \_ ReadPOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpointl)             | Ruft die In einer [**POINTL-Struktur**](/previous-versions//dd162807(v=vs.85)) eines angegebenen Eigenschaftenbehälters gespeicherten Eigenschaftenkoordinaten ab.<br/>    |
| [**\_PSPropertyBag-ReadPOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpoints)             | Ruft die Eigenschaftenkoordinaten ab, die in einer [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) eines angegebenen Eigenschaften bag gespeichert sind.<br/>    |
| [**PSPropertyBag \_ ReadPropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpropertykey)   | Liest den Eigenschaftsschlüssel einer Eigenschaft in einer angegebenen Eigenschaftentüte.<br/>                                                 |
| [**PSPropertyBag \_ ReadRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readrectl)               | Ruft die Koordinaten eines Rechtecks ab, das in einer Eigenschaft gespeichert ist, die in einer angegebenen Eigenschaftentüte enthalten ist.<br/>              |
| [**PSPropertyBag \_ ReadSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readshort)               | Liest den **SHORT-Datenwert** einer Eigenschaft in einer Eigenschaftentüte.<br/>                                                   |
| [**PSPropertyBag \_ ReadStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstr)                   | Liest den **Zeichenfolgendatenwert** einer Eigenschaft in einer Eigenschaftentüte.<br/>                                                  |
| [**PSPropertyBag \_ ReadStrAlloc**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstralloc)         | Liest einen **Zeichenfolgendatenwert** aus einer Eigenschaft in einer Eigenschaftentüte und ordnet Arbeitsspeicher für die gelesene Zeichenfolge zu.<br/> |
| [**PSPropertyBag \_ ReadStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readstream)             | Liest den Datenstrom, der in einer angegebenen Eigenschaft gespeichert ist, die in einer angegebenen Eigenschaftentüte enthalten ist.<br/>                           |
| [**PSPropertyBag \_ ReadType**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readtype)                 | Liest den Typ des Datenwerts einer Eigenschaft, die in einer Eigenschaftentüte gespeichert ist.<br/>                                      |
| [**PSPropertyBag \_ ReadULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readulonglong)       | Liest einen **ULONGLONG-Datenwert** aus einer Eigenschaft in einer Eigenschaftentüte.<br/>                                               |
| [**PSPropertyBag \_ ReadUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readunknown)           | Liest eine bestimmte Eigenschaft eines unbekannten Datenwerts in einer Eigenschaftentüte.<br/>                                                |
| [**PSPropertyBag \_ WriteBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebool)               | Legt den **BOOL-Datenwert** einer Eigenschaft in einem Eigenschaftenbehälter fest.<br/>                                                     |
| [**PSPropertyBag \_ WriteBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebstr)               | Legt einen **BSTR-Datenwert** aus einer Eigenschaft in einem Eigenschaftenbehälter fest.<br/>                                                     |
| [**PSPropertyBag \_ WriteDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writedword)             | Legt einen **DWORD-Datenwert** aus der -Eigenschaft in einem Eigenschaftenbehälter fest.<br/>                                                      |
| [**PSPropertyBag \_ WriteGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeguid)               | Legt den GUID-Datenwert aus einer Eigenschaft in einem Eigenschaftenbehälter fest.<br/>                                                       |
| [**PSPropertyBag \_ WriteInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeint)                 | Legt einen **int-Datenwert** aus einer Eigenschaft in einem Eigenschaftenbehälter fest.<br/>                                                     |
| [**PSPropertyBag \_ WriteLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writelong)               | Legt einen **LONG-Datenwert** aus einer Eigenschaft in einem Eigenschaftenbehälter fest.<br/>                                                     |
| [**PSPropertyBag \_ WritePOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepointl)           | Speichert die Eigenschaftenkoordinaten, die in einer [**POINTL-Struktur**](/previous-versions//dd162807(v=vs.85)) eines angegebenen Eigenschaftenbehälters gespeichert sind.<br/>       |
| [**PSPropertyBag \_ WritePOINTS**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepoints)           | Speichert die Eigenschaftenkoordinaten, die in einer [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) eines angegebenen Eigenschaftenbehälters gespeichert sind.<br/>       |
| [**PSPropertyBag \_ WritePropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepropertykey) | Legt den Eigenschaftenschlüssel einer Eigenschaft in einem angegebenen Eigenschaftenbehälter fest.<br/>                                                  |
| [**PSPropertyBag \_ WriteRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writerectl)             | Speichert die Koordinaten eines Rechtecks, das in einer Eigenschaft gespeichert ist, die in einem angegebenen Eigenschaftenbehälter enthalten ist.<br/>                 |
| [**PSPropertyBag \_ WriteSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeshort)             | Legt den **SHORT-Datenwert** einer Eigenschaft in einem Eigenschaften bag fest.<br/>                                                    |
| [**PSPropertyBag \_ WriteStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestr)                 | Legt den **Zeichenfolgendatenwert** einer Eigenschaft in einem Eigenschaften bag fest.<br/>                                                   |
| [**PSPropertyBag \_ WriteStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestream)           | Legt den Datenstrom fest, der in einer angegebenen Eigenschaft gespeichert ist, die in einer angegebenen Eigenschaftentüte enthalten ist.<br/>                            |
| [**PSPropertyBag \_ WriteULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeulonglong)     | Legt einen **ULONGLONG-Datenwert** aus einer Eigenschaft in einem Eigenschaften bag fest.<br/>                                                |
| [**PSPropertyBag \_ WriteUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeunknown)         | Legt eine bestimmte Eigenschaft eines unbekannten Datenwerts in einem Eigenschaften bag fest.<br/>                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PROPVARIANT und VARIANT (Funktionen)](./functions-propvarutil.md)
</dt> <dt>

[Funktionen](functions.md)
</dt> </dl>

 

 
