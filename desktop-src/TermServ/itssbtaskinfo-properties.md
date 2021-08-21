---
title: ITsSbTaskInfo-Eigenschaften
description: Die ITsSbTaskInfo-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d91b24b95b6b19cb439350c0c6823306c66a8fab5fe47f0f9e9fb739df64e3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128068"
---
# <a name="itssbtaskinfo-properties"></a>ITsSbTaskInfo-Eigenschaften

Die [**ITsSbTaskInfo-Schnittstelle**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) macht die folgenden Eigenschaften verfügbar.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Context-Eigenschaft**](itssbtaskinfo-context.md)
</dt> <dd>

Ruft die kontextbedingten Bytes ab, die der Aufgabe zugeordnet sind.

</dd> <dt>

[**Deadline-Eigenschaft**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

Ruft die Zeit ab, zu der die Aufgabe initiiert werden muss. Dies wird verwendet, um Patches zu priorisieren. Der Patch mit dem frühesten Stichtag wird zuerst initiiert.

</dd> <dt>

[**EndTime-Eigenschaft**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

Ruft die letzte Zeit ab, zu der der Task-Agent den Task starten kann.

</dd> <dt>

[**Eigenschaft Bezeichner**](itssbtaskinfo-identifier.md)
</dt> <dd>

Ruft eine GUID ab, die vom Task-Agent als eindeutiger Bezeichner verwendet wird.

</dd> <dt>

[**Bezeichnung (Eigenschaft)**](itssbtaskinfo-label.md)
</dt> <dd>

Ruft die Bezeichnung ab, die den Zweck der Aufgabe beschreibt.

</dd> <dt>

[**Plug-In-Eigenschaft**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

Ruft den Anzeigenamen des Task-Agents ab.

</dd> <dt>

[**StartTime-Eigenschaft**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

Ruft die früheste Zeit ab, zu der der Task-Agent den Task starten kann.

</dd> <dt>

[**Status-Eigenschaft**](itssbtaskinfo-status.md)
</dt> <dd>

Ruft einen [**RDV \_ TASK \_ STATUS-Enumerationswert**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) ab, der den Zustand der Aufgabe darstellt.

</dd> <dt>

[**TargetId-Eigenschaft**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

Ruft den Zielbezeichner ab.

</dd> </dl>

 

 




