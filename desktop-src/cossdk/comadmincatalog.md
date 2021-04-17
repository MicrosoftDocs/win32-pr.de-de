---
description: Greift auf die Daten zu, die im com+-Katalog gespeichert sind.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Comadmincatalog-Klasse (COMAdmin. h)
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
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483614"
---
# <a name="comadmincatalog-class"></a>Comadmincatalog-Klasse

Greift auf die Daten zu, die im com+-Katalog gespeichert sind.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von com+ implementiert.



| Anforderung | Wert |
|------------|-------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID \_ comadmincatalog                                                                                            |
| ProgID     | L "COMAdmin. comadmincatalog"                                                                                       |
| Schnittstellen | [**Icomadmincatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a>Verwendung

Mithilfe von Objekten, die aus der **comadmincatalog** -Klasse erstellt wurden, können Sie den programmgesteuerten Zugriff auf die im com+-Katalog gespeicherten com+-Konfigurationsdaten starten Diese Informationen unterliegen den Ordnern und Elementen in der Konsolen Struktur des Verwaltungs Tools Komponenten Dienste. Mit der **comadmincatalog** -Klasse können Sie auf Auflistungen im-Katalog zugreifen, com+-Anwendungen und-Komponenten installieren, Dienste starten und starten und eine Verbindung mit Remote Servern herstellen und diese verwalten.

Ordner im Verwaltungs Tool Komponenten Dienste entsprechen Sammlungen im-Katalog, die Sie mithilfe von Objekten darstellen können, die aus der [**comadmincatalogcollection**](comadmincatalogcollection.md) -Klasse erstellt wurden. Elemente in den Ordnern entsprechen Elementen in den Auflistungen, die Sie mithilfe von Objekten darstellen können, die aus der [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse erstellt wurden.

Nicht alle Auflistungen und Elemente, die über " [**comadmincatalogcollection**](comadmincatalogcollection.md) " und " [**COMAdminCatalogObject**](comadmincatalogobject.md) " verfügbar gemacht werden, sind im Verwaltungs Tool für Komponenten Dienste verfügbar.

Informationen zu bestimmten Sammlungen und deren Eigenschaften finden Sie unter [com+-Verwaltungs Sammlungen](com--administration-collections.md).

Eine Einführung in die programmgesteuerte Verwaltung von com+ finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md).

## <a name="remarks"></a>Bemerkungen

Um dieses Objekt zu erstellen, rufen Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)auf.

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die com+-admin-Typbibliothek hinzu. Ein comadmincatalog-Objekt kann mithilfe von "COMAdmin. comadmincatalog" als Klassenname deklariert werden.

In com+ 1,5, das mit Windows XP veröffentlicht wurde, implementiert die **comadmincatalog** -Klasse die [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) -Schnittstelle. In com+ 1,0, veröffentlicht mit Windows 2000, implementiert die **comadmincatalog** -Klasse jedoch nur die [**icomadmincatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) -Schnittstelle.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>"COMAdmin. h"</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>COMAdmin. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Comadmincatalogcollection**](comadmincatalogcollection.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**Icomadmincatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

