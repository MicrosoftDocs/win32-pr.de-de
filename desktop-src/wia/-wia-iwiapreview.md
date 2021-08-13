---
description: Die IWiaPreview-Schnittstelle speichert ungefilterte Bilder intern zwischen und übergibt sie über Bildverarbeitungsfilter.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: IWiaPreview-Schnittstelle (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e2672211e5c1a17fa360a6078069ae8260687dc896843ffb6bf572d9b7be8caa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442070"
---
# <a name="iwiapreview-interface"></a>IWiaPreview-Schnittstelle

Die **IWiaPreview-Schnittstelle** speichert ungefilterte Bilder intern zwischen und übergibt sie über Bildverarbeitungsfilter.

## <a name="members"></a>Member

Die **IWiaPreview-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaPreview** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWiaPreview-Schnittstelle** verfügt über diese Methoden.



| Methode                                                  | Beschreibung                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Klar**](-wia-iwiapreview-clear.md)                 | Gibt das ungefilterte Image frei, das von der [**IWiaPreview::GetNewPreview-Methode zwischengespeichert**](-wia-iwiapreview-getnewpreview.md) wird. Außerdem wird der Bildverarbeitungsfilter veröffentlicht. <br/>          |
| [**DetectRegions**](-wia-iwiapreview-detectregions.md) | Ruft den Treibersegmentierungsfilter auf und übergibt das ungefilterte Bild, das von der [**IWiaPreview::GetNewPreview-Methode**](-wia-iwiapreview-getnewpreview.md) zwischengespeichert wurde, an den Filter. <br/> |
| [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) | Speichert das vom Treiber zurückgegebene ungefilterte Image intern zwischen. <br/>                                                                                                                |
| [**UpdatePreview**](-wia-iwiapreview-updatepreview.md) | Ruft das ungefilterte Bild ab, das von der [**IWiaPreview::GetNewPreview-Methode zwischengespeichert**](-wia-iwiapreview-getnewpreview.md) wird. <br/>                                                            |



 

## <a name="remarks"></a>Hinweise

Dieser Filter wird automatisch von der [**IWiaTransfer::D ownload-Methode**](-wia-iwiatransfer-download.md) aufgerufen.

Die **IWiaPreview-Schnittstelle** erbt wie alle Component Object Model -Schnittstellen (COM) die [IUnknown-Schnittstellenmethoden.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| IUnknown-Methoden                                        | Beschreibung                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
