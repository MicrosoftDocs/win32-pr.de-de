---
description: Greift auf die Daten zu, die im COM+-Katalog gespeichert sind.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: COMAdminCatalog-Klasse (ComAdmin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 8be3f0f3f9aa59c2199c50b73b8a4d4488b0c9a65d3e0679b65350d6b8b07fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128992"
---
# <a name="comadmincatalog-class"></a>COMAdminCatalog-Klasse

Greift auf die Daten zu, die im COM+-Katalog gespeichert sind.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von COM+ implementiert.



| Anforderung | Wert |
|------------|-------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID \_ COMAdminCatalog                                                                                            |
| ProgID     | L"COMAdmin.COMAdminCatalog"                                                                                       |
| Schnittstellen | [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a>Verwendung

Sie verwenden Objekte, die aus der **COMAdminCatalog-Klasse** erstellt wurden, um den programmgesteuerten Zugriff auf com+-Konfigurationsdaten zu starten, die im COM+-Katalog gespeichert sind. Diese Informationen sind den Ordnern und Elementen in der Konsolenstruktur des Component Services-Verwaltungstools zugrunde. Mit **der COMAdminCatalog-Klasse** können Sie auf Sammlungen im Katalog zugreifen, COM+-Anwendungen und -Komponenten installieren, Dienste starten und beenden sowie eine Verbindung mit Remoteservern herstellen und diese verwalten.

Ordner im Component Services-Verwaltungstool entsprechen Sammlungen im Katalog, die Sie mithilfe von Objekten darstellen können, die aus der [**COMAdminCatalogCollection-Klasse**](comadmincatalogcollection.md) erstellt wurden. Elemente in den Ordnern entsprechen Elementen in den Sammlungen, die Sie mithilfe von Objekten darstellen können, die aus der [**COMAdminCatalogObject-Klasse**](comadmincatalogobject.md) erstellt wurden.

Nicht alle Sammlungen und Elemente, die über [**COMAdminCatalogCollection**](comadmincatalogcollection.md) und [**COMAdminCatalogObject**](comadmincatalogobject.md) verfügbar gemacht werden, sind im Component Services-Verwaltungstool verfügbar.

Informationen zu bestimmten Sammlungen und deren Eigenschaften finden Sie unter [COM+-Verwaltungssammlungen.](com--administration-collections.md)

Eine Einführung in die programmgesteuerte Verwaltung von COM+ finden Sie unter [Automatisieren der COM+-Verwaltung.](automating-com--administration.md)

## <a name="remarks"></a>Hinweise

Um dieses Objekt zu erstellen, rufen Sie [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)auf.

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die COM+-Administratortypbibliothek hinzu. Ein COMAdminCatalog-Objekt kann mit "COMAdmin.COMAdminCatalog" als Klassenname deklariert werden.

In COM+ 1.5, veröffentlicht mit Windows XP, implementiert die **COMAdminCatalog-Klasse** die [**ICOMAdminCatalog2-Schnittstelle.**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) In COM+ 1.0, veröffentlicht mit Windows 2000, implementiert die **COMAdminCatalog-Klasse** jedoch nur die [**ICOMAdminCatalog-Schnittstelle.**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>ComAdmin.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin.Idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

