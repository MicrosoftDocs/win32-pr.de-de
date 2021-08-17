---
description: Zielobjekt
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Zielobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b528d66fb789e4d237dacae151c3dda596e834f84f529c3677905672de3b7588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057948"
---
# <a name="target-object"></a>Zielobjekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Ein Zielobjekt modelliert ein iSCSI-Ziel, das in einem iSCSI-Subsystem enthalten ist.

Verwenden Sie [**die IVdsSubSystemIscsi::QueryTargets-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) um die iSCSI-Ziele des Subsystems zu bestimmen. Aufrufer können einen Zeiger auf ein bestimmtes Ziel erhalten, indem sie das gewünschte Zielobjekt aus der -Enumeration auswählen, die von der **QueryTargets-Methode zurückgegeben** wird. Mit einem Zielobjekt können Sie den Benutzerfreundlichen Namen und die Abfrage des Ziels für Zieleigenschaften, zugeordnete LUNs und das Subsystem festlegen, das das Ziel enthält.

Hostcomputer müssen sich bei Zielen anmelden, um auf ihre zugeordneten LUNs zugreifen zu können. Um eine Anmeldung bei einem Ziel durchzuführen, muss dem Ziel mindestens ein Portal in einer seiner Portalgruppen zugeordnet sein. Eingaben und Ausgaben von zugeordneten LUNs werden über diese Anmeldesitzung verarbeitet.

Zielobjekteigenschaften umfassen einen Objektbezeichner, einen iSCSI-Namen, einen Bezeichnernamen und ein CHAP-fähiges Flag.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.



| type                                                                                      | Element                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer nur in ISCSI-Anbietern der Version 1.1 und 2.0 verfügbar gemacht werden | [**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).                                                                                 |
| Zugeordnete Enumerationen                                                                   | Keine.                                                                                                                       |
| Zugeordnete Strukturen                                                                     | [**VDS \_ \_ \_ ISCSI-ZIEL-PROP-**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) [**UND \_ VDS-ZIELBENACHRICHTIGUNG. \_**](/windows/desktop/api/Vds/ns-vds-vds_target_notification) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardwareanbieterobjekte](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
