---
description: Die iwiatransfercallback-Schnittstelle empfängt Rückrufe während einer Datenübertragung.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Iwiatransfercallback-Schnittstelle (WIA. h)
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
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129409"
---
# <a name="iwiatransfercallback-interface"></a>Iwiatransfercallback-Schnittstelle

Die **iwiatransfercallback** -Schnittstelle empfängt Rückrufe während einer Datenübertragung.

## <a name="members"></a>Member

Die **iwiatransfercallback** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwiatransfercallback** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwiatransfercallback** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**Getnextstream**](-wia-iwiatransfercallback-getnextstream.md)       | Ruft einen neuen Stream für das angegebene Element ab. <br/>                    |
| [**Transfercallback**](-wia-iwiatransfercallback-transfercallback.md) | Gibt den Fortschritt und andere Benachrichtigungen während einer Übertragung an. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Bild Verarbeitungs Filter-Entwickler sollten diese Schnittstelle und die [**iwiaimagefilter**](-wia-iwiaimagefilter.md) -Schnittstelle implementieren.

Die **iwiatransfercallback** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.



| IUnknown-Methoden                                        | BESCHREIBUNG                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown:: adressf](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
