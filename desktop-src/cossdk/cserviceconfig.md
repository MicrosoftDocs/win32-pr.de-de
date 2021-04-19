---
description: Gibt die Dienste an, die in der Dienst Domäne aktiv sein sollen, die beim Aufrufen von cocreateactivity oder coenterservicedomain eingegeben werden soll, und konfiguriert diese.
ms.assetid: f546ded4-255e-4565-b588-f36175902778
title: Cserviceconfig-Klasse (Comsvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CServiceConfig
api_type:
- COM
ms.openlocfilehash: e0b48b05be4afa1d42dbc8a16c4b596a08aba859
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346433"
---
# <a name="cserviceconfig-class"></a>Cserviceconfig-Klasse

Gibt die Dienste an, die in der Dienst Domäne aktiv sein sollen, die beim Aufrufen von [**cocreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) oder [**coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)eingegeben werden soll, und konfiguriert diese.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID \_ cserviceconfig                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ProgID     | L "Comsvcs. Cserviceconfig "                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Schnittstellen | [**Iservicecomtiintrinsicsconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [**Iserviceiisintrinsicsconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [**Iserviceingeerbanceconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [**Iservicepartitionconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [**Iservicesxsconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [**Iservicesynchronizationconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [**Iservicethreadpoolconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [**Iservicetrackerconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [**Iservicetransaktionconfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um die Dienste zu konfigurieren, die Sie verwenden möchten. Mit [**cokreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) und [**coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) können Sie die von dieser Klasse konfigurierten Dienste verwenden, ohne diese Dienste vor der Verwendung an eine Komponente binden zu müssen.

Diese Klasse wurde nicht für die Verwendung in Visual Basic konzipiert.

## <a name="remarks"></a>Bemerkungen

Um dieses Objekt zu erstellen, rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)auf.

Objekte, die von der **cserviceconfig** -Klasse instanziiert werden, Aggregieren den Freethread-Mars Haller, sodass Sie von System Laufzeiten gespeichert und in unterschiedlichen Apartments wieder verwendet werden können.

Um einen einzelnen Dienst zu konfigurieren, wird [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die dem Dienst zugeordnete-Schnittstelle aufgerufen und dann Methoden für diese Schnittstelle aufgerufen, um die entsprechende Konfiguration einzurichten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>"Comsvcs. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cokreateactivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[**Cokreatefreethreadedmarshaler**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)
</dt> <dt>

[**Coenterservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**Coleaveservicedomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[Com+-Dienste ohne Komponenten](com--services-without-components.md)
</dt> </dl>

 

