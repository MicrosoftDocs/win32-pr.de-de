---
description: Die iwiatransfer-Schnittstelle stellt Datenstrom basierte Übertragung von Daten bereit.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Iwiatransfer-Schnittstelle (WIA. h)
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
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214651"
---
# <a name="iwiatransfer-interface"></a>Iwiatransfer-Schnittstelle

Die **iwiatransfer** -Schnittstelle stellt Datenstrom basierte Übertragung von Daten bereit.

## <a name="members"></a>Member

Die **iwiatransfer** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwiatransfer** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwiatransfer** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Abbrechen**](-wia-iwiatransfer-cancel.md)                             | Bricht den aktuellen Übertragungsvorgang ab. <br/>                                         |
| [**Herunterladen**](-wia-iwiatransfer-download.md)                         | Initiiert einen Daten Download für den Aufrufer. <br/>                                        |
| [**Enumwia- \_ Format \_ Informationen**](-wia-iwiatransfer-enumwia-format-info.md) | Erstellt einen Enumerator für die Übertragungs Formate, die das WIA 2,0-Gerät unterstützt.<br/> |
| [**Upload**](-wia-iwiatransfer-upload.md)                             | Initiiert einen Daten Upload eines einzelnen Elements vom Aufrufer. <br/>                       |



 

## <a name="remarks"></a>Bemerkungen

Die **iwiatransfer** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.



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



 

 
