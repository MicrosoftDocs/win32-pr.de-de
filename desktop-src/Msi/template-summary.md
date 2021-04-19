---
description: Bei einem Installationspaket gibt die Eigenschaft Vorlagen Zusammenfassung die Plattform-und Sprachversionen an, die mit dieser Installations Datenbank kompatibel sind.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Vorlagen Zusammenfassungs Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373682"
---
# <a name="template-summary-property"></a>Vorlagen Zusammenfassungs Eigenschaft

Bei einem Installationspaket gibt die Eigenschaft **Vorlagen Zusammenfassung** die Plattform-und Sprachversionen an, die mit dieser Installations Datenbank kompatibel sind. Die Syntax der Eigenschaften Informationen für die **Vorlagen Zusammenfassung** für eine Installations Datenbank lautet wie folgt:

\[*Platt Form Eigenschaft* \] ; \[ *Sprach-ID* \] \[ ,*Sprach-ID* \] \[ ,... \] .

Die folgenden Beispiele sind gültige Werte für die Eigenschaft **Vorlagen Zusammenfassung** :

-   x64; 1033
-   Intel; 1033
-   Intel64; 1033
-   ; 1033
-   Intel; 1033, 2046
-   Intel64; 1033, 2046
-   Intel; 0
-   Arm; 1033, 2046
-   Arm; 0
-   Arm64; 1033, 2046
-   Arm64; 0

Die **Vorlagen Zusammenfassungs** Eigenschaft einer Transformation gibt die Plattform-und Sprachversionen an, die mit der Transformation kompatibel sind. In einer Transformations Datei kann nur eine Sprache angegeben werden. Die angegebene Plattform und Sprache bestimmen, ob eine Transformation auf eine bestimmte Datenbank angewendet werden kann. Die Platform-Eigenschaft und die Language-Eigenschaft können leer gelassen werden, wenn keine Transformations Einschränkung zur Validierung der Transformation erforderlich ist.

Die **Vorlagen Zusammenfassungs** Eigenschaft eines Patchpakets ist eine durch Semikolons getrennte Liste der Produktcodes, die den Patch akzeptieren können. Wenn Sie [Msimsp.exe](msimsp-exe.md) und [Patchwiz.dll](patchwiz-dll.md) verwenden, um das Patchpaket zu generieren, wird diese Liste aus der [TargetImages-Tabelle](targetimages-table-patchwiz-dll-.md) der patcherstellungs-Datei abgerufen.

Diese Zusammenfassungs Eigenschaft ist erforderlich.

## <a name="remarks"></a>Bemerkungen

Wenn die aktuelle Plattform nicht mit einer der in der **Vorlagen Zusammenfassungs** Eigenschaft angegebenen Plattformen identisch ist, wird das Paket vom Installationsprogramm nicht verarbeitet.

Wenn die Platt Form Spezifikation im Eigenschafts Wert für die **Vorlagen Zusammenfassung** fehlt, nimmt das Installationsprogramm die Intel-Architektur an.

Wenn es sich um ein 64-Bit-Windows Installer Paket handelt, das auf einer Itanium-Plattform (Intel64) ausgeführt wird, geben Sie in der Eigenschaft **Vorlagen Zusammenfassung** Intel64 ein.

Wenn es sich um ein 64-Bit-Windows Installer Paket handelt, das auf einer x64-Plattform ausgeführt wird, geben Sie x64 in der Eigenschaft **Vorlagen Zusammenfassung** ein.

Wenn es sich um ein 64-Bit-Windows Installer Paket handelt, das auf einer Arm64-Plattform ausgeführt wird, geben Sie in der Eigenschaft **Vorlagen Zusammenfassung** Arm64 ein.

Ein Windows Installer Paket kann nicht als Unterstützung sowohl für Intel64 als auch für x64 gekennzeichnet werden. Beispielsweise ist der Wert für die **Vorlagen Zusammenfassungs** Eigenschaft Intel64, x64 ungültig.

Ein Windows Installer Paket kann nicht als Unterstützung für 32-Bit-und 64-Bit-Plattformen gekennzeichnet werden. Beispielsweise sind **Vorlagen Zusammenfassungs** Eigenschaftswerte wie Intel, x64 oder Intel, Intel64 ungültig.

Wenn Sie im Feld "Sprache-ID" der Eigenschaft " **Vorlagen Zusammenfassung** " den Wert 0 (null) eingeben oder dieses Feld leer gelassen wird, wird angegeben, dass das Paket sprachneutral ist.

Wenn dies ein Windows Installer Paket ist, das unter Windows RT ausgeführt wird, geben Sie den Wert Arm in der Eigenschaft **Vorlagen Zusammenfassung** ein.

Mergemodule sind die einzigen Pakete, die mehrere Sprachen aufweisen können. In einer quellinstallerdatenbank kann nur eine Sprache angegeben werden. Weitere Informationen finden Sie unter [mehrere sprachmergemodule](multiple-language-merge-modules.md).

Die Alpha Plattform wird von Windows Installer nicht unterstützt.

**Windows Installer:** Die folgende Syntax wird nicht unterstützt:

\[*Platt Form Eigenschaft* \] \[ ,*Platt Form Eigenschaft* \] \[ ,... \] \[ *Sprach-ID* \] \[ ,*Sprach-ID* \] \[ ,... \] .

Die folgenden Beispiele sind keine gültigen Werte für die **Vorlagen Zusammenfassungs** Eigenschaft:

-   Alpha, Intel; 1033
-   Intel, Alpha; 1033
-   Alpha; 1033
-   Alpha; 1033, 2046

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beschreibungen der Zusammenfassungs Eigenschaften](summary-property-descriptions.md)
</dt> </dl>

 

 




