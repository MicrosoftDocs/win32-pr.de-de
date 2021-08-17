---
title: INapComponentInfo-Schnittstelle (NapCommon.h)
description: Stellt Methoden bereit, die Plug-In-Komponenten (z. B. SHAs und SHVs) implementieren müssen, damit das NAP-System mit ihnen kommunizieren kann.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- INapComponentInfo-Schnittstelle NAP
- INapComponentInfo-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188aae04ab407c5ae26e1d1a764e9093cc101cbe7d714ef8a8e0146013fefee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799705"
---
# <a name="inapcomponentinfo-interface"></a>INapComponentInfo-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapComponentInfo-Schnittstelle** stellt Methoden bereit, die Plug-In-Komponenten (z. B. SHAs und SHVs) implementieren müssen, damit das NAP-System mit ihnen kommunizieren kann. Das NAP-System ruft Ihre Implementierung dieser Methoden auf, um statische Administrative Informationen abzurufen (z. B. Anzeigename oder lokalisierte Zeichenfolgen).

## <a name="members"></a>Member

Die **INapComponentInfo-Schnittstelle erbt** von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapComponentInfo** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapComponentInfo-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                         | BESCHREIBUNG                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**INapComponentInfo::ConvertErrorCodeToMessageId**](inapcomponentinfo-converterrorcodetomessageid-method.md) | Wird vom NAP-System verwendet, um anzufordern, dass der Integritätsclient einen HRESULT-Fehlercode in eine Meldungs-ID konvertiert.<br/> |
| [**INapComponentInfo::GetDescription**](inapcomponentinfo-getdescription-method.md)                           | Wird vom NAP-System verwendet, um die Beschreibung eines Integritätsclients abzurufen.<br/>                                  |
| [**INapComponentInfo::GetFriendlyName**](inapcomponentinfo-getfriendlyname-method.md)                         | Wird vom NAP-System verwendet, um den Anzeigenamen eines Integritätsclients abzurufen.<br/>                                |
| [**INapComponentInfo::GetIcon**](inapcomponentinfo-geticon-method.md)                                         | Wird vom NAP-System verwendet, um das Symbol eines Integritätsclients abzurufen.<br/>                                         |
| [**INapComponentInfo::GetLocalizedString**](inapcomponentinfo-getlocalizedstring-method.md)                   | Wird vom NAP-System verwendet, um lokalisierte Zeichenfolgen abzurufen.<br/>                                                   |
| [**INapComponentInfo::GetVendorName**](inapcomponentinfo-getvendorname-method.md)                             | Wird vom NAP-System verwendet, um den Herstellernamen eines Integritätsclients abzurufen.<br/>                                  |
| [**INapComponentInfo::GetVersion**](inapcomponentinfo-getversion-method.md)                                   | Wird vom NAP-System verwendet, um die Version eines Integritätsclients abzurufen.<br/>                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

