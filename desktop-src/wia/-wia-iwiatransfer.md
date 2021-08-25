---
description: Die IWiaTransfer-Schnittstelle ermöglicht die streambasierte Übertragung von Daten.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: IWiaTransfer-Schnittstelle (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: ff19619b1f0ab46658d0876792248befd6940c525d5c7da1b3331f6ca1a8c12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813900"
---
# <a name="iwiatransfer-interface"></a>IWiaTransfer-Schnittstelle

Die **IWiaTransfer-Schnittstelle** ermöglicht die streambasierte Übertragung von Daten.

## <a name="members"></a>Member

Die **IWiaTransfer-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaTransfer** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWiaTransfer-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Abbrechen**](-wia-iwiatransfer-cancel.md)                             | Bricht den aktuellen Übertragungsvorgang ab. <br/>                                         |
| [**Herunterladen**](-wia-iwiatransfer-download.md)                         | Initiiert einen Datendownload an den Aufrufer. <br/>                                        |
| [**EnumWIA \_ FORMAT \_ INFO**](-wia-iwiatransfer-enumwia-format-info.md) | Erstellt einen Enumerator für die Übertragungsformate, die das WIA 2.0-Gerät unterstützt.<br/> |
| [**Upload**](-wia-iwiatransfer-upload.md)                             | Initiiert einen Datenupload eines einzelnen Elements vom Aufrufer. <br/>                       |



 

## <a name="remarks"></a>Hinweise

Die **IWiaTransfer-Schnittstelle** erbt wie alle Component Object Model -Schnittstellen (COM) die [IUnknown-Schnittstellenmethoden.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| IUnknown-Methoden                                        | BESCHREIBUNG                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
