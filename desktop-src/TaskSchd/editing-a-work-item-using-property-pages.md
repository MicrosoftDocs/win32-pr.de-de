---
title: Bearbeiten eines Arbeitselements mithilfe von Eigenschaftenseiten
description: Sie können die Eigenschaften eines Arbeitselements mithilfe der grafischen Benutzeroberfläche bearbeiten, die vom Taskplaner wird.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- Bearbeiten von Arbeitselementen Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0121a9e3100922ecdd1d529aa81b498d377724959abb5c3380337df82817e338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100430"
---
# <a name="editing-a-work-item-using-property-pages"></a>Bearbeiten eines Arbeitselements mithilfe von Eigenschaftenseiten

Sie können die Eigenschaften eines Arbeitselements mithilfe der grafischen Benutzeroberfläche bearbeiten, die vom Taskplaner wird. (Derzeit sind die einzigen gültigen Arbeitselemente Aufgaben.)

Im folgenden Verfahren wird beschrieben, wie Sie einen Task mithilfe seiner Eigenschaftenseiten bearbeiten.

**So bearbeiten Sie eine Aufgabe mithilfe ihrer Eigenschaftenseiten**

1.  Rufen [**Sie CoInitialize auf,**](/windows/win32/api/objbase/nf-objbase-coinitialize) um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner zu erhalten. (In diesen Beispielen wird davon ausgegangen, Taskplaner dienst ausgeführt wird.)
2.  Rufen [**Sie ITaskScheduler::Activate auf,**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) des Aufgabenobjekts zu erhalten. (Beachten Sie, dass Tasks derzeit der einzige gültige Typ von Arbeitselement sind.)
3.  Rufen [**Sie IScheduledWorkItem::EditWorkItem auf,**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) um die Eigenschaftenseiten für die Aufgabe anzuzeigen.
4.  Bearbeiten Sie die Eigenschaften der Aufgabe nach Bedarf, und klicken Sie dann auf OK, um die neuen Werte zu akzeptieren und die angezeigten Eigenschaftenseiten zu entfernen.



| Ein Codebeispiel für                                                                                      | Siehe                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Anzeigen der Eigenschaftenseiten für eine bekannte Aufgabe und Zulassen, dass ein Benutzer die Eigenschaften des Arbeitselements bearbeiten kann | [C/C++-Codebeispiel: Bearbeiten eines Arbeitselements](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1.0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 