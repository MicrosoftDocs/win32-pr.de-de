---
description: Die Eigenschaft Keywords Summary in Installationsdatenbanken oder Transformationen enthält eine Liste von Schlüsselwörtern.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Eigenschaft "Keywords Summary"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a572161e440b440010d43f598e2baa453dbca514d71aa6f0f672deb7c726fa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680310"
---
# <a name="keywords-summary-property"></a>Eigenschaft "Keywords Summary"

Die **Eigenschaft Keywords Summary** in Installationsdatenbanken oder Transformationen enthält eine Liste von Schlüsselwörtern. Die Schlüsselwörter können von Dateibrowsern verwendet werden, um Schlüsselwortsuchen nach einer Datei durchzuführen. Diese Eigenschaft enthält eine Liste der Quellen des Patches in einem Patchpaket.

Der Autor einer Installationsdatenbank, einer Transformation oder eines Patchpakets muss den Wert dieser Eigenschaft in den Zusammenfassungsinformationen angeben. Autoren sollten folgende Schritte ausführen, um den richtigen Wert zu bestimmen.

-   Legen Sie in einem Installationspaket den Wert dieser Eigenschaft auf eine Liste von Schlüsselwörtern fest. Das Schlüsselwort sollte "Installer" sowie produktspezifische Schlüsselwörter enthalten und kann lokalisiert werden.
-   Legen Sie in einer Transformation den Wert dieser Eigenschaft auf eine Liste von Schlüsselwörtern fest. Das Schlüsselwort sollte "Installer" sowie produktspezifische Schlüsselwörter enthalten und kann lokalisiert werden.
-   Legen Sie in einem Patchpaket den Wert dieser Eigenschaft auf eine durch Semikolons getrennte Liste von Netzwerk- oder URL-Speicherorten für die Quellen des Patches fest. Wenn der Patch installiert ist, fügt das Installationsprogramm diese der Quellliste für das Patchpaket hinzu. Wenn der zwischengespeicherte Patch fehlt, kann das Installationsprogramm mithilfe der Funktionen [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) oder [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) nach einer Quelle am ursprünglichen Speicherort suchen, einen Speicherort, der der Quellliste durch die **Eigenschaft Zusammenfassung** der Schlüsselwörter hinzugefügt wurde, oder nach einem Speicherort, der der Quellliste hinzugefügt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zusammenfassungseigenschaftenbeschreibungen](summary-property-descriptions.md)
</dt> </dl>

 

 




