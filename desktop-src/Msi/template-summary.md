---
description: Bei einem Installationspaket gibt die Eigenschaft Vorlagenzusammenfassung die Plattform- und Sprachversionen an, die mit dieser Installationsdatenbank kompatibel sind.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Template Summary-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da93d2d3a38f3c1853f3f936fe6f97b8550dcaeac70d4b553b8cb0362f41ee41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893450"
---
# <a name="template-summary-property"></a>Template Summary-Eigenschaft

Bei einem Installationspaket gibt die **Eigenschaft Vorlagenzusammenfassung** die Plattform- und Sprachversionen an, die mit dieser Installationsdatenbank kompatibel sind. Die Syntax der Eigenschafteninformationen der **Vorlagenzusammenfassung** für eine Installationsdatenbank lautet wie folgt:

\[*platform-Eigenschaft* \] ; \[ *Sprach-ID,* \] \[ *Sprach-ID* \] \[ ,... \] .

Die folgenden Beispiele sind gültige Werte für die **Eigenschaft Vorlagenzusammenfassung:**

-   x64;1033
-   Intel;1033
-   Intel64;1033
-   ;1033
-   Intel ;1033,2046
-   Intel64;1033,2046
-   Intel;0
-   Arm;1033,2046
-   Arm;0
-   Arm64;1033,2046
-   Arm64;0

Die **Template Summary-Eigenschaft** einer Transformation gibt die Plattform- und Sprachversionen an, die mit der Transformation kompatibel sind. In einer Transformationsdatei kann nur eine Sprache angegeben werden. Die angegebene Plattform und Sprache bestimmen, ob eine Transformation auf eine bestimmte Datenbank angewendet werden kann. Die Plattformeigenschaft und die Spracheigenschaft können leer gelassen werden, wenn keine Transformationseinschränkung von ihnen abhängt, um die Transformation zu überprüfen.

Die **Template Summary-Eigenschaft** eines Patchpakets ist eine durch Semikolons getrennte Liste der Produktcodes, die den Patch akzeptieren können. Wenn Sie [Msimsp.exe](msimsp-exe.md) und [Patchwiz.dll](patchwiz-dll.md) verwenden, um das Patchpaket zu generieren, wird diese Liste aus der [Tabelle TargetImages](targetimages-table-patchwiz-dll-.md) der Patcherstellungsdatei abgerufen.

Diese Zusammenfassungseigenschaft ist erforderlich.

## <a name="remarks"></a>Hinweise

Wenn die aktuelle Plattform nicht mit einer der in der **Eigenschaft Vorlagenzusammenfassung** angegebenen Plattformen übereinstimmt, verarbeitet das Installationsprogramm das Paket nicht.

Wenn die Plattformspezifikation im Eigenschaftswert **Vorlagenzusammenfassung** fehlt, geht das Installationsprogramm von der Intel-Architektur aus.

Wenn es sich um ein 64-Bit-Windows Installer-Paket handelt, das auf einer Intel64-Plattform (Itanium) ausgeführt wird, geben Sie Intel64 in die Eigenschaft **Vorlagenzusammenfassung** ein.

Wenn es sich um ein 64-Bit-Windows Installer-Paket handelt, das auf einer x64-Plattform ausgeführt wird, geben Sie x64 in die **Eigenschaft Vorlagenzusammenfassung** ein.

Wenn es sich um ein 64-Bit-Windows Installer-Paket handelt, das auf einer Arm64-Plattform ausgeführt wird, geben Sie Arm64 in die Eigenschaft **Vorlagenzusammenfassung** ein.

Ein Windows Installer-Paket kann nicht als Unterstützung für Intel64 und x64 markiert werden. Beispielsweise ist der Template **Summary-Eigenschaftswert** von Intel64,x64 ungültig.

Ein Windows Installer-Paket kann nicht als Unterstützung für 32-Bit- und 64-Bit-Plattformen markiert werden. Beispielsweise sind Eigenschaftswerte der **Vorlagenzusammenfassung** wie Intel, x64 oder Intel,Intel64 ungültig.

Wenn Sie 0 (null) in das Sprach-ID-Feld der **Eigenschaft Vorlagenzusammenfassung** eingeben oder dieses Feld leer lassen, bedeutet dies, dass das Paket sprachneutral ist.

Wenn es sich um ein Windows Installer-Paket handelt, das auf Windows RT ausgeführt wird, geben Sie in der Eigenschaft **Vorlagenzusammenfassung** den Wert Arm ein.

Mergemodule sind die einzigen Pakete, die mehrere Sprachen aufweisen können. In einer Quellinstallationsdatenbank kann nur eine Sprache angegeben werden. Weitere Informationen finden Sie unter [Multiple Language Merge Modules](multiple-language-merge-modules.md).

Die Alphaplattform wird von Windows Installer nicht unterstützt.

**Windows Installer:** Die folgende Syntax wird nicht unterstützt:

\[*platform-Eigenschaft,* \] \[ *Plattformeigenschaft* \] \[ ,... \] \[ *Sprach-ID,* \] \[ *Sprach-ID* \] \[ ,... \] .

Die folgenden Beispiele sind keine gültigen Werte für die **Eigenschaft Vorlagenzusammenfassung:**

-   Alpha, Intel;1033
-   Intel,Alpha;1033
-   Alpha;1033
-   Alpha;1033,2046

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Zusammenfassungseigenschaftenbeschreibungen](summary-property-descriptions.md)
</dt> </dl>

 

 




