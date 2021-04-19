---
description: Dieser Abschnitt enthält eine Liste der WMI-Rückgabecodes, symbolischen Konstanten, Literalwerte und Beschreibungen. Diese Codes können von Skripts, C++-Anwendungen oder WMIC-Befehlen zurückgegeben werden.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: WMI-Rückgabe Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348878"
---
# <a name="wmi-return-codes"></a>WMI-Rückgabe Codes

Dieser Abschnitt enthält eine Liste der WMI-Rückgabecodes, symbolischen Konstanten, Literalwerte und Beschreibungen. Diese Codes können von Skripts, C++-Anwendungen oder [**WMIC**](wmic.md) -Befehlen zurückgegeben werden.

Wenn ein Fehler auftritt, gibt WMI einen der folgenden Fehlercodes als 32-Bit-Wert zurück, wobei die zwei höherwertigen Bits den Schweregrad Code der Nachricht angeben.

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

<span id="3"></span>€
</dt> <dd>

Fehler

</dd> </dl>

> [!Note]
>
> Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass Sie möglicherweise nicht auf Probleme im WMI-Dienst oder in WMI-Anbietern hinweisen. Fehler können aus anderen Teilen des Betriebssystems stammen und als Fehler über WMI auftreten. Löschen Sie das WMI-Repository unter Umständen nicht als erste Aktion, da das Löschen des Repository zu Beschädigungen des Systems oder der installierten Anwendungen führen kann.
>
> Um weitere Informationen zur Ursache des Problems zu erhalten, können Sie das Befehlszeilen Tool [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Diagnose herunterladen und ausführen. Mit diesem Tool wird ein Bericht erstellt, der in der Regel die Ursache des Problems isolieren und Anweisungen zur Behebung des Problems bereitstellen kann. Der Bericht hilft Ihnen auch bei der Unterstützung durch den Microsoft-Support. Sie können die WMI-Diagnosehilfsprogramm [hier](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)herunterladen.

 

-   [**WMI-Fehler Konstanten**](wmi-error-constants.md)
-   [**WMI-nicht-Fehler-Konstanten**](wmi-non-error-constants.md)

 

 



