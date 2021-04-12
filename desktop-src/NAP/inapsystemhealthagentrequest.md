---
title: Inapsystemhealthagentrequest-Schnittstelle (napsystemhealthagent. h)
description: SHAs verwenden Sie, um die Verarbeitung mit dem NAP-System zu kommunizieren und zu koordinieren.
ms.assetid: 424e0fb7-cce7-4b75-b474-fda0e053284e
keywords:
- Inapsystemhealthagentrequest-Schnittstelle NAP
- Inapsystemhealthagentrequest-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e79e2a6347ebffec37595d4ca86b100830047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517705"
---
# <a name="inapsystemhealthagentrequest-interface"></a>Inapsystemhealthagentrequest-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentrequest** -Schnittstelle stellt Methoden bereit, die von SHAs zum kommunizieren und koordinieren der Verarbeitung mit dem NAP-System verwendet werden.

## <a name="members"></a>Member

Die **inapsystemhealthagentrequest** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapsystemhealthagentrequest** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapsystemhealthagentrequest** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                                     | BESCHREIBUNG                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**Inapsystemhealthagentrequest:: getcachesohflag**](inapsystemhealthagentrequest-getcachesohflag-method.md)               | Wird nur von NAPAgent verwendet.<br/>                                                            |
| [**Inapsystemhealthagentrequest:: getcorrelationid**](inapsystemhealthagentrequest-getcorrelationid-method.md)             | Wird von Systemintegritäts-Agents verwendet, um SoHs und [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh)zu korrelieren.<br/> |
| [**Inapsystemhealthagentrequest:: getsohrequest**](inapsystemhealthagentrequest-getsohrequest-method.md)                   | Wird von SHAs verwendet, um SoHs zu erhalten, die zuvor vom NAPAgent zwischengespeichert wurden.<br/>                           |
| [**Inapsystemhealthagentrequest:: getsohresponse**](inapsystemhealthagentrequest-getsohresponse-method.md)                 | Wird vom Integritäts-Agent zum Abrufen der [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh)verwendet.<br/>         |
| [**Inapsystemhealthagentrequest:: getstringcorrelationid**](inapsystemhealthagentrequest-getstringcorrelationid-method.md) | Wird von Systemintegritäts-Agents zum Protokollieren der Korrelations-ID verwendet<br/>                               |
| [**Inapsystemhealthagentrequest:: setsohrequest**](inapsystemhealthagentrequest-setsohrequest-method.md)                   | Wird von Health-Agents zum Schreiben der SoH-Anforderung verwendet.<br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napsystemhealthagent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthagent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

