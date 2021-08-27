---
description: Stellt die Dateiversionsverlauf-Konfiguration des Benutzers dar, unter dem das -Objekt Von DerConfigMgr erstellt wird. Alle Konfigurationsvorgänge werden durch Aufrufen der Methoden der IFhConfigMgr-Schnittstelle ausgeführt.
ms.assetid: CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788
title: SollenconfigMgr-Klasse (Kscfg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhConfigMgr
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 700e96b72e3b23fa83a384a68bd2723ae244d69b0b10ed47db10843793166f40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058970"
---
# <a name="fhconfigmgr-class"></a>Automatischer Konfigurations-Mgr-Klasse

Stellt die Dateiversionsverlauf-Konfiguration des Benutzers dar, unter dem das **-Objekt Von DerConfigMgr** erstellt wird. Alle Konfigurationsvorgänge werden durch Aufrufen der Methoden der [**IFhConfigMgr-Schnittstelle**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) ausgeführt.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Die Dateiversionsverlauf-API implementiert diese Klasse. Um eine Instanz dieser Klasse zu erstellen, verwenden Sie die [**CoCreateInstance-Funktion.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Wgcfg.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wgcfg.idl</dt> </dl> |



 

 
