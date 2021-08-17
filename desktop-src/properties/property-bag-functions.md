---
description: In diesem Abschnitt wird eine Reihe von Hilfsfunktionen Windows, die mit IPropertyBag-Objekten verwendet werden.
ms.assetid: 4ef85855-7eb6-43ec-bf29-1223eaf1a0cc
title: Eigenschaften-Bag-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b33bdcced7c030a476a3ec303ac30b5c5d0f722bceea5358678ba1a2fe6f790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970939"
---
# <a name="property-bag-functions"></a>Eigenschaften-Bag-Funktionen

In diesem Abschnitt wird eine Reihe von hilfsfunktionen Windows, die mit [**IPropertyBag-Objekten verwendet**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) werden.



| Thema                                                                       | Inhalte                                                                                                                     |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PSPropertyBag \_ Delete**](/windows/win32/api/propsys/nf-propsys-pspropertybag_delete)                     | Löscht eine Eigenschaft aus einer Eigenschaftentüte.<br/>                                                                           |
| [**PSPropertyBag \_ ReadBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbool)                 | Liest den **BOOL-Datenwert** einer Eigenschaft in einem Eigenschaften bag.<br/>                                                    |
| [**PSPropertyBag \_ ReadBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readbstr)                 | Liest einen **BSTR-Datenwert** aus einer Eigenschaft in einer Eigenschaftentüte.<br/>                                                    |
| [**PSPropertyBag \_ ReadDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readdword)               | Liest einen **DWORD-Datenwert** aus der -Eigenschaft in einer Eigenschaftentüte.<br/>                                                     |
| [**PSPropertyBag \_ ReadGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readguid)                 | Liest den GUID-Datenwert aus einer Eigenschaft in einer Eigenschaftentüte.<br/>                                                      |
| [**PSPropertyBag \_ ReadInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readint)                   | Liest einen **int-Datenwert** aus einer Eigenschaft in einer Eigenschaftentüte.<br/>                                                    |
| [**PSPropertyBag \_ ReadLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readlong)                 | Liest einen **LONG-Datenwert** aus einer Eigenschaft in einer Eigenschaftentüte.<br/>                                                    |
| [**PSPropertyBag \_ ReadPOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_readpointl)             | Ruft die Eigenschaftenkoordinaten ab, die in einer [**POINTL-Struktur**](/previous-versions//dd162807(v=vs.85)) eines angegebenen Eigenschaftentschlags gespeichert sind.<br/>    |
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
| [**PSPropertyBag \_ WriteBOOL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebool)               | Legt den **BOOL-Datenwert** einer Eigenschaft in einem Eigenschaftentüt fest.<br/>                                                     |
| [**PSPropertyBag \_ WriteBSTR**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writebstr)               | Legt einen **BSTR-Datenwert** aus einer Eigenschaft in einer Eigenschaftentüte fest.<br/>                                                     |
| [**PSPropertyBag \_ WriteDWORD**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writedword)             | Legt einen **DWORD-Datenwert** aus der -Eigenschaft in einem Eigenschaftentüt fest.<br/>                                                      |
| [**PSPropertyBag \_ WriteGUID**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeguid)               | Legt den GUID-Datenwert aus einer Eigenschaft in einem Eigenschaften bag fest.<br/>                                                       |
| [**PSPropertyBag \_ WriteInt**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeint)                 | Legt einen **int-Datenwert** aus einer Eigenschaft in einem Eigenschaftentüt fest.<br/>                                                     |
| [**PSPropertyBag \_ WriteLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writelong)               | Legt einen **LONG-Datenwert** aus einer Eigenschaft in einem Eigenschaften bag fest.<br/>                                                     |
| [**PSPropertyBag \_ WritePOINTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepointl)           | Speichert die Eigenschaftenkoordinaten, die in einer [**POINTL-Struktur**](/previous-versions//dd162807(v=vs.85)) eines angegebenen Eigenschaftentschlags gespeichert sind.<br/>       |
| [**\_PSPropertyBag-SchreibPUNKTE**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepoints)           | Speichert die Eigenschaftenkoordinaten, die in einer [**POINTS-Struktur**](/previous-versions//dd162808(v=vs.85)) eines angegebenen Eigenschaften bag gespeichert sind.<br/>       |
| [**PSPropertyBag \_ WritePropertyKey**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writepropertykey) | Legt den Eigenschaftsschlüssel einer Eigenschaft in einer angegebenen Eigenschaftentüte fest.<br/>                                                  |
| [**PSPropertyBag \_ WriteRECTL**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writerectl)             | Speichert die Koordinaten eines Rechtecks, das in einer Eigenschaft gespeichert ist, die in einer angegebenen Eigenschaftentüte enthalten ist.<br/>                 |
| [**PSPropertyBag \_ WriteSHORT**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeshort)             | Legt den **SHORT-Datenwert** einer Eigenschaft in einem Eigenschaften bag fest.<br/>                                                    |
| [**PSPropertyBag \_ WriteStr**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestr)                 | Legt den **Zeichenfolgendatenwert** einer Eigenschaft in einem Eigenschaftentüt fest.<br/>                                                   |
| [**PSPropertyBag \_ WriteStream**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writestream)           | Legt den Datenstrom fest, der in einer angegebenen Eigenschaft gespeichert ist, die in einer angegebenen Eigenschaftentüte enthalten ist.<br/>                            |
| [**PSPropertyBag \_ WriteULONGLONG**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeulonglong)     | Legt einen **ULONGLONG-Datenwert** aus einer Eigenschaft in einer Eigenschaftentüte fest.<br/>                                                |
| [**PSPropertyBag \_ WriteUnknown**](/windows/win32/api/propsys/nf-propsys-pspropertybag_writeunknown)         | Legt eine bestimmte Eigenschaft eines unbekannten Datenwerts in einer Eigenschaftentüte fest.<br/>                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PROPVARIANT und VARIANT (Funktionen)](./functions-propvarutil.md)
</dt> <dt>

[Funktionen](functions.md)
</dt> </dl>

 

 
