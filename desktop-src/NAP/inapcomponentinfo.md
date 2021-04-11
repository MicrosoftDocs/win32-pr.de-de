---
title: Inapcomponentinfo-Schnittstelle (napcommon. h)
description: Stellt Methoden bereit, die von Plug-in-Komponenten (z. b. SHAs und SHVs) implementiert werden müssen, damit das NAP-System mit Ihnen kommuniziert.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- Inapcomponentinfo-Schnittstelle NAP
- Inapcomponentinfo-Schnittstelle NAP, beschrieben
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
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949670"
---
# <a name="inapcomponentinfo-interface"></a>Inapcomponentinfo-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapcomponentinfo** -Schnittstelle stellt Methoden bereit, die von Plug-in-Komponenten (z. b. SHAs und SHVs) implementiert werden müssen, damit das NAP-System mit Ihnen kommuniziert. Das NAP-System ruft Ihre Implementierung dieser Methoden auf, um statische administrative Informationen (z. b. Anzeige Name oder lokalisierte Zeichen folgen) abzurufen.

## <a name="members"></a>Member

Die **inapcomponentinfo** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapcomponentinfo** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapcomponentinfo** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                         | BESCHREIBUNG                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Inapcomponentinfo:: converterrorcodetomess ageid**](inapcomponentinfo-converterrorcodetomessageid-method.md) | Wird vom NAP-System verwendet, um anzufordern, dass der Integritäts Client einen HRESULT-Fehlercode in eine Nachrichten-ID konvertiert.<br/> |
| [**Inapcomponentinfo:: GetDescription**](inapcomponentinfo-getdescription-method.md)                           | Wird vom NAP-System verwendet, um die Beschreibung eines Integritäts Clients zu erhalten.<br/>                                  |
| [**Inapcomponentinfo:: getfriendlyname**](inapcomponentinfo-getfriendlyname-method.md)                         | Wird vom NAP-System verwendet, um den anzeigen Amen eines Integritäts Clients zu erhalten.<br/>                                |
| [**Inapcomponentinfo:: getIcon**](inapcomponentinfo-geticon-method.md)                                         | Wird vom NAP-System verwendet, um das Symbol eines Integritäts Clients zu erhalten.<br/>                                         |
| [**Inapcomponentinfo:: GetLocalizedString**](inapcomponentinfo-getlocalizedstring-method.md)                   | Wird vom NAP-System verwendet, um lokalisierte Zeichen folgen zu erhalten.<br/>                                                   |
| [**Inapcomponentinfo:: getvendorname**](inapcomponentinfo-getvendorname-method.md)                             | Wird vom NAP-System verwendet, um den Herstellernamen eines Integritäts Clients zu erhalten.<br/>                                  |
| [**Inapcomponentinfo:: GetVersion**](inapcomponentinfo-getversion-method.md)                                   | Wird vom NAP-System verwendet, um die Version eines Integritäts Clients zu erhalten.<br/>                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

