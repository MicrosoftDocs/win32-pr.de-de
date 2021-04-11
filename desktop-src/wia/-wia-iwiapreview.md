---
description: Die iwiapreview-Schnittstelle speichert ungefilterte Bilder intern zwischen und übergibt sie durch Bild Verarbeitungs Filter.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Iwiapreview-Schnittstelle (WIA. h)
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
ms.openlocfilehash: 5e1c01daae4e86fa18c087b67bf902daaf6f8793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214655"
---
# <a name="iwiapreview-interface"></a>Iwiapreview-Schnittstelle

Die **iwiapreview** -Schnittstelle speichert ungefilterte Bilder intern zwischen und übergibt sie durch Bild Verarbeitungs Filter.

## <a name="members"></a>Member

Die **iwiapreview** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwiapreview** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwiapreview** -Schnittstelle verfügt über diese Methoden.



| Methode                                                  | BESCHREIBUNG                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Klartext**](-wia-iwiapreview-clear.md)                 | Gibt das ungefilterte Bild frei, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird. Außerdem wird der Bild Verarbeitungs Filter freigegeben. <br/>          |
| [**DetectRegions**](-wia-iwiapreview-detectregions.md) | Ruft den Treiber Segmentierungs Filter auf und übergibt das ungefilterte Bild, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird, an den Filter. <br/> |
| [**Getnewpreview**](-wia-iwiapreview-getnewpreview.md) | Speichert das vom Treiber zurückgegebene ungefilterte Bild intern zwischen. <br/>                                                                                                                |
| [**Updatepreview**](-wia-iwiapreview-updatepreview.md) | Ruft das ungefilterte Bild ab, das von der [**iwiapreview:: getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode zwischengespeichert wird. <br/>                                                            |



 

## <a name="remarks"></a>Bemerkungen

Dieser Filter wird automatisch von der [**iwiatransfer::D ownload**](-wia-iwiatransfer-download.md) -Methode aufgerufen.

Die **iwiapreview** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.



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



 

 
