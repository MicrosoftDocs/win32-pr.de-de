---
description: Die IWiaSegmentationFilter-Schnittstelle erkennt Unterbereiche eines Bilddatenstroms und macht jeweils separate IWiaItem2-Elemente.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: IWiaSegmentationFilter-Schnittstelle (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 304b5be43aad8afc1730d2a23c170f11f11d319ffc4ae3eb13781efe09da2d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659700"
---
# <a name="iwiasegmentationfilter-interface"></a>IWiaSegmentationFilter-Schnittstelle

Die **IWiaSegmentationFilter-Schnittstelle** erkennt Unterbereiche eines Bilddatenstroms und macht jeweils separate [**IWiaItem2-Elemente.**](-wia-iwiaitem2.md)

## <a name="members"></a>Member

Die **IWiaSegmentationFilter-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaSegmentationFilter** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWiaSegmentationFilter-Schnittstelle** verfügt über diese Methoden.



| Methode                                                             | Beschreibung                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) | Bestimmt die Unterbereiche eines Bilds, das auf dem flachen Nummernschild angeordnet ist, sodass jeder untere Bereich in einem separaten Bildelement erworben werden kann. <br/> |



 

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) verwenden, um eine neue Instanz des Segmentierungsfilters zu erstellen. Eine Anwendung ruft diese Funktion in der Regel auf, bevor ihr Vorschaufenster angezeigt wird.

Verwenden Sie beim Implementieren dieses Filters [**IWiaItem2::CreateChildItem,**](-wia-iwiaitem2-createchilditem.md) um die untergeordneten Elemente zu erstellen. Die Anwendung sollte **COPY \_ PARENT PROPERTY \_ \_ VALUES** an den *ICreationFlags-Parameter* übergeben, um sicherzustellen, dass Eigenschaften wie Bildformat und Auflösung im neu erstellten untergeordneten Element identisch sind wie im übergeordneten Element.

Ein Segmentierungsfilter muss alle Bildformate unterstützen, die der Treiber unterstützt, mit dem er verwendet wird. Der von Microsoft bereitgestellte Filter unterstützt Bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) und Tagged Image File Format (TIFF).

Der Segmentierungsfilter sollte nur für Film- und Flatbedscannerelemente verwendet werden. Bei der Filmüberprüfung enthält ein Scanner häufig feste Frames. In diesem Fall hat der Treiber die untergeordneten Elemente erstellt, und die Anwendung sollte den Segmentierungsfilter nicht aufrufen.

Die **IWiaSegmentationFilter-Schnittstelle** erbt wie alle COM-Schnittstellen (Component Object Model) die [IUnknown-Schnittstellenmethoden.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| IUnknown-Methoden                                        | Beschreibung                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
