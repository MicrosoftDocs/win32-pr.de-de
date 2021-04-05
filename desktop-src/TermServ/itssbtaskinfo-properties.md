---
title: Itssbtaskinfo-Eigenschaften
description: Die itssbtaskinfo-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718282"
---
# <a name="itssbtaskinfo-properties"></a>Itssbtaskinfo-Eigenschaften

Die [**itssbtaskinfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Context-Eigenschaft**](itssbtaskinfo-context.md)
</dt> <dd>

Ruft die dem Task zugeordneten Kontext Bytes ab.

</dd> <dt>

[**Stichtag (Eigenschaft)**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

Ruft den Zeitpunkt ab, zu dem die Aufgabe initiiert werden muss. Hiermit werden Patches priorisiert. Der Patch mit dem frühesten Stichtag wird zuerst initiiert.

</dd> <dt>

[**EndTime (Eigenschaft)**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

Ruft den letzten Zeitpunkt ab, zu dem der Task-Agent den Task starten kann.

</dd> <dt>

[**Eigenschaft Bezeichner**](itssbtaskinfo-identifier.md)
</dt> <dd>

Ruft eine GUID ab, die vom Task-Agent als eindeutiger Bezeichner verwendet wird.

</dd> <dt>

[**Bezeichnung (Eigenschaft)**](itssbtaskinfo-label.md)
</dt> <dd>

Ruft die Bezeichnung ab, die den Zweck der Aufgabe beschreibt.

</dd> <dt>

[**Plugin-Eigenschaft**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

Ruft den anzeigen amen des Task-Agents ab.

</dd> <dt>

[**StartTime (Eigenschaft)**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

Ruft den frühesten Zeitpunkt ab, zu dem der Task-Agent den Task starten kann.

</dd> <dt>

[**Status (Eigenschaft)**](itssbtaskinfo-status.md)
</dt> <dd>

Ruft einen RDV-aufgabenstatusenumerationswert ab, der den Zustand der Aufgabe darstellt. [**\_ \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)

</dd> <dt>

[**TargetID-Eigenschaft**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

Ruft den Ziel Bezeichner ab.

</dd> </dl>

 

 




