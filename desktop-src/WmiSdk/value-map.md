---
description: Eine Werte Zuordnung ist ein Array, das mit einer Eigenschaft mit dem Wert und den ValueMap-Qualifizierern verknüpft ist.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: ValueMap-und Wert Qualifizierer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356297"
---
# <a name="valuemap-and-value-qualifiers"></a>ValueMap-und Wert Qualifizierer

Eine Werte Zuordnung ist ein Array, das mit einer Eigenschaft mit dem **Wert** und den **ValueMap** -Qualifizierern verknüpft ist.

Die-Eigenschaft fungiert als Index für das Array, das einen Wert enthält, der einen der Werte im Array darstellt. Mithilfe von MOF-Code können Sie über die folgenden Typen von Wert Maps verfügen:

-   Array Zuordnung zu einer Ganzzahl.

    Sie können ein Array mit dem **Wert** Qualifizierer definieren und das Array direkt mit einer ganzzahligen Eigenschaft verknüpfen, wie im folgenden Beispiel gezeigt:

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    In diesem Beispiel ist der **Status** -Eigenschafts Wert ein Index in das durch den **Wert** definierte Zeichen folgen Array. Die-Eigenschaft kann nur Werte verwenden, die den Ordinalpositionen im **Wert** Array minus 1 entsprechen. Wenn Sie z. b. **Status** auf "1" festlegen, wird der Wert "Error" (Fehler) zugeordnet. Die Index-Eigenschaft kann nur Werte annehmen, die den Positionen im **Wert** Array entsprechen. Wenn das Array z. b. 10 Einträge enthält, kann die Index-Eigenschaft die Story 0 bis 9, nicht 30 oder 177.

-   Array Zuordnung zu einem anderen Array, das einer Ganzzahl entspricht.

    Wenn Sie einen Index erstellen möchten, der kein ordinales System der Zählung verwendet, verwenden Sie den **ValueMap** -Qualifizierer. Der **ValueMap** -Qualifizierer richtet ein anderes Array ein, das ein beliebiges Index Nummerierungssystem enthält, wie im folgenden Beispiel gezeigt:

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    Obwohl Sie die Werte von **ValueMap** in Anführungszeichen platzieren müssen, berücksichtigt WMI die Werte Ganzzahlen. Daher können Sie in diesem Beispiel die Eigenschaft **Status** auf eine Ganzzahl im **ValueMap** -Satz festlegen: 1, 3, 99 oder 0. WMI ordnet jede Ganzzahl von einer Ordinalposition im **ValueMap** -Zeichen folgen Array einer entsprechenden Position im **Werte** Array zu. Wenn Sie z. b. **Status** auf 0 festlegen, wird "unbekannt" zugeordnet.

-   Array Zuordnung zu einer anderen Array Zuordnung zu einer Zeichenfolge.

    Wenn Sie keine Ganzzahl zum Indizieren Ihres Arrays verwenden möchten, können Sie stattdessen eine Zeichenfolge verwenden, um einen der möglichen Werte in Ihrem Array zu speichern. Zu diesem Zweck müssen Sie sowohl ein **value** -als auch ein **ValueMap** -Array definieren, das beide Zeichen folgen enthält, wie im folgenden Beispiel gezeigt:

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    Bei einer Zeichen folgen Eigenschaft sind die tatsächlichen zulässigen Werte der Eigenschaft die Einträge im **ValueMap** -Array. Beispielsweise können Sie den **Status** auf "OK" oder "unbekannt" festlegen.

Es liegt in der Anwendung, die Zuordnungen auf nützliche Weise zu nutzen. Der Anbieter muss einen gültigen Wertebereich erzwingen.

## <a name="remarks"></a>Bemerkungen

Wenn Sie entscheiden, ob Sie den **ValueMap**- / **Wert** oder **Bitmap**- / **BitValues** -Qualifizierer verwenden möchten, stellen Sie fest, ob einer der aufgeführten Werte gleichzeitig auftreten könnte. Wenn mehrere gleichzeitige Werte vorhanden sein können, müssen **Bitmap**- / **Bitwerte** verwendet werden. Wenn sich alle Werte gegenseitig ausschließen, sollten Sie die **ValueMap**- / **Wert** Qualifizierer verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bitmap und BitValues](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



