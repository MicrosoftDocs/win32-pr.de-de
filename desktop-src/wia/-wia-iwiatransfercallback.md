---
description: Die IWiaTransferCallback-Schnittstelle empfängt Rückrufe während einer Datenübertragung.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: IWiaTransferCallback-Schnittstelle (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 20c577530785de3e05d00d4674556fbcd03cb69832b164e12dc703108d23c58a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549640"
---
# <a name="iwiatransfercallback-interface"></a>IWiaTransferCallback-Schnittstelle

Die **IWiaTransferCallback-Schnittstelle** empfängt Rückrufe während einer Datenübertragung.

## <a name="members"></a>Member

Die **IWiaTransferCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaTransferCallback** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWiaTransferCallback-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                 | Beschreibung                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md)       | Ruft einen neuen Stream für das angegebene Element ab. <br/>                    |
| [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) | Stellt den Fortschritt und andere Benachrichtigungen während einer Übertragung bereit. <br/> |



 

## <a name="remarks"></a>Hinweise

Entwickler von Bildverarbeitungsfiltern sollten diese Schnittstelle und die [**IWiaImageFilter-Schnittstelle**](-wia-iwiaimagefilter.md) implementieren.

Die **IWiaTransferCallback-Schnittstelle** erbt wie alle com-Schnittstellen (Component Object Model) die [IUnknown-Schnittstellenmethoden.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| IUnknown-Methoden                                        | Beschreibung                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
