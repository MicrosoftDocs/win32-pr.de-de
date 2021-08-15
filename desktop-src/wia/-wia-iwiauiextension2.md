---
description: Die IWiaUIExtension2-Schnittstelle stellt Methoden bereit, die die vom System bereitgestellte Standard-Benutzeroberfläche durch eine benutzerdefinierte Benutzeroberfläche ersetzen und ein benutzerdefiniertes Gerätesymbol bereitstellen.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: IWiaUIExtension2-Schnittstelle (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 2111c25a83a9b826f4cab7dba8f689e01a9868ac416b8fb3026f1b1fb49a90ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208143"
---
# <a name="iwiauiextension2-interface"></a>IWiaUIExtension2-Schnittstelle

Die IWiaUIExtension2-Schnittstelle stellt Methoden bereit, die die vom System bereitgestellte Standard-Benutzeroberfläche durch eine benutzerdefinierte Benutzeroberfläche ersetzen und ein benutzerdefiniertes Gerätesymbol bereitstellen. Gerätehersteller können diese Schnittstelle implementieren, um benutzerdefinierte Benutzeroberflächen für ihre Geräte zur Verfügung zu stellen.

## <a name="members"></a>Member

Die **IWiaUIExtension2-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaUIExtension2** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWiaUIExtension2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**DeviceDialog**](-wia-iwiauiextension2-devicedialog.md)   | Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die Standard-Benutzeroberfläche des Systems ersetzt.<br/> |
| [**GetDeviceIcon**](-wia-iwiauiextension2-getdeviceicon.md) | Ruft ein benutzerdefiniertes Gerätesymbol ab.<br/>                                                        |



 

## <a name="remarks"></a>Hinweise



| IUnknown-Methoden                                        | BESCHREIBUNG                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 
