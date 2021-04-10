---
description: Die iwiasegmentationfilter-Schnittstelle erkennt Unterbereiche eines bildstreams und stellt separate IWiaItem2 Items für jede dar.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Iwiasegmentationfilter-Schnittstelle (WIA. h)
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
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862675"
---
# <a name="iwiasegmentationfilter-interface"></a>Iwiasegmentationfilter-Schnittstelle

Die **iwiasegmentationfilter** -Schnittstelle erkennt Unterbereiche eines bildstreams und stellt separate [**IWiaItem2**](-wia-iwiaitem2.md) Items für jede dar.

## <a name="members"></a>Member

Die **iwiasegmentationfilter** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwiasegmentationfilter** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwiasegmentationfilter** -Schnittstelle verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) | Bestimmt die Unterbereiche eines Bilds, das auf dem flachen Platen angeordnet ist, sodass jede Unterregion in einem separaten Bildelement abgerufen werden kann. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) verwenden, um eine neue Instanz des Segmentierungs Filters zu erstellen. Eine Anwendung ruft diese Funktion in der Regel auf, bevor das Vorschaufenster angezeigt wird.

Verwenden Sie bei der Implementierung dieses Filters [**IWiaItem2:: kreatechilditem**](-wia-iwiaitem2-createchilditem.md) , um die untergeordneten Elemente zu erstellen. Die Anwendung sollte die **Eigenschaften \_ \_ \_ Werte der übergeordneten Kopie** an den *ikreationflags* -Parameter übergeben, um sicherzustellen, dass Eigenschaften wie das Bildformat und die Auflösung in dem neu erstellten untergeordneten Element identisch sind, wie im übergeordneten Element.

Ein Segmentierungs Filter muss alle Bildformate unterstützen, mit denen der Treiber, mit dem er verwendet wird, unterstützt. Der von Microsoft bereitgestellte Filter unterstützt Bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) und Tagged Image File Format (TIFF).

Der Segmentierungs Filter sollte nur für Filterelemente verwendet werden. Bei der Überprüfung des Filters kommt es bei einem Scanner häufig zu festgelegten Rahmen. in diesem Fall hat der Treiber die untergeordneten Elemente erstellt, und die Anwendung sollte den Segmentierungs Filter nicht aufrufen.

Die **iwiasegmentationfilter** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.



| IUnknown-Methoden                                        | BESCHREIBUNG                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown:: adressf](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
