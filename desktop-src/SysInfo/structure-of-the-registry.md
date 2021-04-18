---
description: Die Registrierung ist eine hierarchische Datenbank, die Daten enthält, die für den Betrieb von Windows und die Anwendungen und Dienste, die unter Windows ausgeführt werden, wichtig sind.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Struktur der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b76b7f827ae3ea96d75d089c7d874c3d31d030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555543"
---
# <a name="structure-of-the-registry"></a>Struktur der Registrierung

Die Registrierung ist eine hierarchische Datenbank, die Daten enthält, die für den Betrieb von Windows und die Anwendungen und Dienste, die unter Windows ausgeführt werden, wichtig sind. Die Daten sind in einem Struktur Format strukturiert. Jeder Knoten in der Struktur wird als *Schlüssel* bezeichnet. Jeder Schlüssel kann sowohl *Unterschlüssel* als auch Dateneinträge mit dem Namen *Values* enthalten. Manchmal handelt es sich bei dem vorhanden sein eines Schlüssels um alle Daten, die für eine Anwendung erforderlich sind. in anderen Zeiten öffnet eine Anwendung einen Schlüssel und verwendet die Werte, die dem Schlüssel zugeordnet sind. Ein Schlüssel kann eine beliebige Anzahl von Werten aufweisen, und die Werte können in beliebiger Form vorliegen. Weitere Informationen finden Sie unter [Registrierungs Werttypen](registry-value-types.md) und [Größenbeschränkungen für Registrierungs Elemente](registry-element-size-limits.md).

Jeder Schlüssel weist einen Namen auf, der aus einem oder mehreren druckbaren Zeichen besteht. Bei Schlüsselnamen wird Groß-/Kleinschreibung nicht beachtet. Schlüsselnamen dürfen keinen umgekehrten Schrägstrich enthalten ( \) , es kann jedoch ein beliebiges anderes druckbares Zeichen verwendet werden. Wertnamen und-Daten können den umgekehrten Schrägstrich enthalten.

Der Name jedes unter Schlüssels ist in Bezug auf den Schlüssel, der sich direkt oberhalb des Schlüssels in der Hierarchie befindet, eindeutig. Schlüsselnamen sind nicht in anderen Sprachen lokalisiert, auch wenn die Werte lauten.

Die folgende Abbildung ist ein Beispiel für eine Registrierungsschlüssel Struktur, die im Registrierungs-Editor angezeigt wird.

![Fenster des Registrierungs-Editors](images/regtree.png)

Jede Struktur unter **Arbeitsplatz** ist ein Schlüssel. Der Schlüssel **des \_ lokalen \_ HKEY** -Computers verfügt über die folgenden Unterschlüssel: **Hardware**, **Sam**, **Security**, **Software** und **System**. Alle diese Schlüssel haben wiederum Unterschlüssel. Der **Hardware** Schlüssel weist beispielsweise die Unterschlüssel **Beschreibung**, **DeviceMap** und **ResourceMap** auf. der **DeviceMap** -Schlüssel verfügt über mehrere Unterschlüssel, einschließlich **Video**.

Jeder Wert besteht aus einem Wertnamen und den zugehörigen Daten, sofern vorhanden. " **Maxobjectnumber** " und " **vgacompatible** " sind Werte, die Daten unter dem **Video** Unterschlüssel enthalten.

Eine Registrierungs Struktur kann 512 Ebenen tief sein. Sie können bis zu 32 Ebenen gleichzeitig über einen einzigen Registrierungs-API-Aufruf erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Windows-Registrierung](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))
</dt> </dl>

 

 
