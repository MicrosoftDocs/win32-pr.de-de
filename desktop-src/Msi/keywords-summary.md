---
description: Die Schlüsselwort Zusammenfassungs Eigenschaft in den Installations Datenbanken oder Transformationen enthält eine Liste von Schlüsselwörtern.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Schlüsselwort Zusammenfassungs Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3828146fef861cd993331045d6a1380d84c2bbc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362017"
---
# <a name="keywords-summary-property"></a>Schlüsselwort Zusammenfassungs Eigenschaft

Die **Schlüsselwort Zusammenfassungs** Eigenschaft in den Installations Datenbanken oder Transformationen enthält eine Liste von Schlüsselwörtern. Die Schlüsselwörter können von Datei Browsern verwendet werden, um Schlüsselwörter nach einer Datei zu suchen. Diese Eigenschaft enthält eine Liste der Quellen des Patches in einem Patchpaket.

Es liegt an der Erstellung einer Installations Datenbank, einer Transformation oder eines Patchpakets, um den Wert dieser Eigenschaft in den Zusammenfassungs Informationen bereitzustellen. Autoren sollten die folgenden Schritte ausführen, um den richtigen Wert zu bestimmen.

-   Legen Sie in einem Installationspaket den Wert dieser Eigenschaft auf eine Liste von Schlüsselwörtern fest. Das Schlüsselwort sollte "Installer" und produktspezifische Schlüsselwörter enthalten und möglicherweise lokalisiert werden.
-   Legen Sie in einer Transformation den Wert dieser Eigenschaft auf eine Liste von Schlüsselwörtern fest. Das Schlüsselwort sollte "Installer" und produktspezifische Schlüsselwörter enthalten und möglicherweise lokalisiert werden.
-   Legen Sie in einem Patchpaket den Wert dieser Eigenschaft auf eine durch Semikolons getrennte Liste von Netzwerk-oder URL-Speicherorten für die Quellen des Patches fest. Wenn der Patch installiert ist, fügt das Installationsprogramm diese der Quell Liste für das Patchpaket hinzu. Wenn der zwischengespeicherte Patch fehlt, kann das Installationsprogramm eine Quelle am ursprünglichen Speicherort, einen Speicherort, der der Quell Liste von der **Schlüsselwort Zusammenfassungs** Eigenschaft hinzugefügt wurde, oder einen Speicherort, der der Quell Liste mithilfe der [**msisourcelistaddsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) -Funktion oder der [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) -Funktion hinzugefügt wird, suchen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beschreibungen der Zusammenfassungs Eigenschaften](summary-property-descriptions.md)
</dt> </dl>

 

 




