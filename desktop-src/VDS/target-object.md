---
description: Zielobjekt
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Zielobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1e81ea94a2f608378eba069defc83a721e0fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352726"
---
# <a name="target-object"></a>Zielobjekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Zielobjekt modelliert ein iSCSI-Ziel, das in einem iSCSI-Subsystem enthalten ist.

Verwenden Sie die [**ivdssubsystemiscsi:: querytargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) -Methode, um die iSCSI-Ziele des Subsystems zu ermitteln. Aufrufer können einen Zeiger auf ein bestimmtes Ziel abrufen, indem Sie das gewünschte Zielobjekt aus der-Enumeration auswählen, das von der **querytargets** -Methode zurückgegeben wird. Mit einem Zielobjekt können Sie den anzeigen amen des Ziels festlegen und die Zieleigenschaften, zugeordneten LUNs und das Subsystem, das das Ziel enthält, Abfragen.

Host Computer müssen sich bei Zielen anmelden, damit Sie auf die zugehörigen LUNs zugreifen können. Um eine Anmeldung bei einem Ziel durchzuführen, muss das Ziel mindestens über ein zugeordnetes Portal in einer der zugehörigen Portal Gruppen verfügen. Eingaben und Ausgaben von zugeordneten LUNs werden über diese Anmelde Sitzung behandelt.

Zu den Zielobjekt Eigenschaften gehören ein Objekt Bezeichner, ein iSCSI-Name, ein Anzeige Name und ein CHAP-aktiviertes Flag.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                                                                      | Element                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer nur in VDS 1,1-und 2,0-iSCSI-Anbietern verfügbar gemacht werden | [**Ivdsiscsitarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).                                                                                 |
| Zugehörige Enumerationen                                                                   | Keine.                                                                                                                       |
| Zugeordnete Strukturen                                                                     | [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) Ziel-und [**VDS- \_ Ziel \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_target_notification)für iSCSI-Ziel. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hardware Anbieter Objekte](hardware-provider-objects.md)
</dt> <dt>

[**Ivdssubsystemiscsi:: querytargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
