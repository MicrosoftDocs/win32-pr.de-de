---
description: Dieser Abschnitt enthält eine Liste der WMI-Rückgabecodes, symbolischen Konstanten, Literalwerte und Beschreibungen. Diese Codes können von Skripts, C++-Anwendungen oder Wmic-Befehlen zurückgegeben werden.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: WMI-Rückgabecodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1454c8efc45085e88f78358346679b5cdcf3d05093318845912d7d5a913d8ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995380"
---
# <a name="wmi-return-codes"></a>WMI-Rückgabecodes

Dieser Abschnitt enthält eine Liste der WMI-Rückgabecodes, symbolischen Konstanten, Literalwerte und Beschreibungen. Diese Codes können von Skripts, C++-Anwendungen oder [**Wmic-Befehlen zurückgegeben**](wmic.md) werden.

Wenn ein Fehler auftritt, gibt WMI einen der folgenden Fehlercodes als 32-Bit-Wert zurück, wobei die beiden hochwertigen Bits den Schweregradcode der Nachricht angeben.

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Erfolg

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Informational

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

Warnung

</dd> <dt>

<span id="3"></span>3
</dt> <dd>

Fehler

</dd> </dl>

> [!Note]
>
> Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass sie möglicherweise nicht auf Probleme im WMI-Dienst oder in WMI-Anbietern hinweisen. Fehler können aus anderen Teilen des Betriebssystems stammen und über WMI als Fehler auftreten. Löschen Sie das WMI-Repository unter keinen Umständen als erste Aktion, da das Löschen des Repositorys schäden am System oder an installierten Anwendungen verursachen kann.
>
> Um weitere Informationen zur Problemquelle zu erhalten, können Sie das Befehlszeilentool WMI-Diagnosehilfsprogramm [Diagnose](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) herunterladen und ausführen. Dieses Tool erstellt einen Bericht, der normalerweise die Ursache des Problems isolieren und Anweisungen zum Beheben des Problems bereitstellen kann. Der Bericht unterstützt Auch Microsoft-Supportdienste bei der Unterstützung. Sie können die Datei WMI-Diagnosehilfsprogramm [hier herunterladen.](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)

 

-   [**WMI-Fehlerkonst constants**](wmi-error-constants.md)
-   [**Nicht-Fehler-WMI-Konstanten**](wmi-non-error-constants.md)

 

 



