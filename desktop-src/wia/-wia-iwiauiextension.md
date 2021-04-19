---
description: Die iwiauiextension-Schnittstelle stellt Methoden bereit, die die standardmäßige Systembenutzer Oberfläche ersetzen, ein benutzerdefiniertes Geräte Bitmap-Logo bereitstellen und ein benutzerdefiniertes Gerätesymbol bereitstellen.
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: Iwiauiextension-Schnittstelle (wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 98318ba3b2b94d334834150b219c5d453c4e0d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348415"
---
# <a name="iwiauiextension-interface"></a>Iwiauiextension-Schnittstelle

Die **iwiauiextension** -Schnittstelle stellt Methoden bereit, die die standardmäßige Systembenutzer Oberfläche ersetzen, ein benutzerdefiniertes Geräte Bitmap-Logo bereitstellen und ein benutzerdefiniertes Gerätesymbol bereitstellen.

## <a name="members"></a>Member

Die **iwiauiextension** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwiauiextension** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwiauiextension** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Devicedialog**](-wia-iwiauiextension-devicedialog.md)               | Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.<br/> |
| [**Getdevicebitmaplogo**](-wia-iwiauiextension-getdevicebitmaplogo.md) | Ruft ein benutzerdefiniertes bitmaplogo für das Gerät ab.<br/>                                         |
| [**Getde viceicon**](-wia-iwiauiextension-getdeviceicon.md)             | Ruft ein benutzerdefiniertes Gerätesymbol ab.<br/>                                                        |



 

## <a name="remarks"></a>Bemerkungen



| IUnknown-Methoden                                        | BESCHREIBUNG                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown:: adressf](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 
