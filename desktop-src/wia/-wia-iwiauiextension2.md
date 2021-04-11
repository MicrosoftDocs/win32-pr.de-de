---
description: Die IWiaUIExtension2-Schnittstelle stellt Methoden bereit, die die vom System bereitgestellte Standardbenutzer Oberfläche durch eine benutzerdefinierte Benutzeroberfläche ersetzen und ein benutzerdefiniertes Gerätesymbol bereitstellen.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: IWiaUIExtension2-Schnittstelle (wiadevd. h)
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
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958969"
---
# <a name="iwiauiextension2-interface"></a>IWiaUIExtension2-Schnittstelle

Die IWiaUIExtension2-Schnittstelle stellt Methoden bereit, die die vom System bereitgestellte Standardbenutzer Oberfläche durch eine benutzerdefinierte Benutzeroberfläche ersetzen und ein benutzerdefiniertes Gerätesymbol bereitstellen. Gerätehersteller können diese Schnittstelle implementieren, um benutzerdefinierte Benutzeroberflächen für Ihre Geräte bereitzustellen.

## <a name="members"></a>Member

Die **IWiaUIExtension2** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IWiaUIExtension2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWiaUIExtension2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Devicedialog**](-wia-iwiauiextension2-devicedialog.md)   | Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.<br/> |
| [**Getde viceicon**](-wia-iwiauiextension2-getdeviceicon.md) | Ruft ein benutzerdefiniertes Gerätesymbol ab.<br/>                                                        |



 

## <a name="remarks"></a>Bemerkungen



| IUnknown-Methoden                                        | BESCHREIBUNG                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Gibt Zeiger auf unterstützte Schnittstellen zurück. |
| [IUnknown:: adressf](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Inkrementiert Verweiszähler.               |
| [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Dekrementiert Verweiszähler.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 
