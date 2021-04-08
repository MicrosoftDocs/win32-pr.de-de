---
title: Bearbeiten eines Arbeits Elements mithilfe von Eigenschaften Seiten
description: Sie können die Eigenschaften eines Arbeits Elements bearbeiten, indem Sie die grafische Benutzeroberfläche verwenden, die vom Taskplaner-Dienst bereitgestellt wird.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- Bearbeiten von Arbeits Elementen Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0958c361f1c076e8ebed6a7e645bf67694a1d01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727985"
---
# <a name="editing-a-work-item-using-property-pages"></a>Bearbeiten eines Arbeits Elements mithilfe von Eigenschaften Seiten

Sie können die Eigenschaften eines Arbeits Elements bearbeiten, indem Sie die grafische Benutzeroberfläche verwenden, die vom Taskplaner-Dienst bereitgestellt wird. (Zurzeit sind die einzigen gültigen Arbeitselemente Tasks.)

Im folgenden Verfahren wird beschrieben, wie eine Aufgabe mithilfe ihrer Eigenschaften Seiten bearbeitet wird.

**So bearbeiten Sie eine Aufgabe mithilfe der zugehörigen Eigenschaften Seiten**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesen Beispielen wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen. (Beachten Sie, dass Aufgaben derzeit der einzige gültige Typ von Arbeits Element sind.)
3.  Aufrufen von [**ischeduledworkitem:: editworkitem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) , um die Eigenschaften Seiten für den Task anzuzeigen.
4.  Bearbeiten Sie die Eigenschaften der Aufgabe nach Bedarf, und klicken Sie dann auf OK, um die neuen Werte zu übernehmen und die angezeigten Eigenschaften Seiten zu entfernen.



| Ein Codebeispiel für                                                                                      | Siehe                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Anzeigen der Eigenschaften Seiten für eine bekannte Aufgabe und ermöglichen der Bearbeitung der Eigenschaften der Arbeitsaufgabe durch einen Benutzer | [C/C++-Code Beispiel: Bearbeiten eines Arbeits Elements](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 