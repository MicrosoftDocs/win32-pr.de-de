---
description: ICE56 überprüft, ob die Verzeichnisstruktur der .msi-Datei über ein einzelnes Stammverzeichnis verfügt, dass der Stamm die TARGETDIR-Eigenschaft ist und dass sich der SourceDir-Eigenschaftswert in der DefaultDir-Spalte der Directory-Tabelle befindet.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c1feb3e3dbab84a58809496b28a60d3a2436c3041d3a2d58f0ac8f2b5e47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528220"
---
# <a name="ice56"></a>ICE56

ICE56 überprüft, ob die Verzeichnisstruktur der .msi-Datei über ein einzelnes Stammverzeichnis verfügt, dass der Stamm die [**TARGETDIR-Eigenschaft**](targetdir.md) ist und dass sich der [**SourceDir-Eigenschaftswert**](sourcedir.md) in der DefaultDir-Spalte der [Verzeichnistabelle](directory-table.md)befindet.

Wenn eine .msi Datei mehrere Stammdateien enthält oder einen anderen Stamm als [**TARGETDIR**](targetdir.md)angibt, wird bei einer [Administratorinstallation](administrative-installation.md) kein korrektes Administratorimage erstellt.

Beachten Sie, dass leere Verzeichnisse nicht von ICE56 überprüft werden. Die Verzeichnisstruktur besteht die Überprüfung mit mehreren Stammverzeichnissen, wenn die zusätzlichen Verzeichnisse leer sind.

## <a name="result"></a>Ergebnis

ICE56 gibt einen Fehler aus, wenn die .msi keinen einzelnen Stamm ( [**TARGETDIR**](targetdir.md)) hat oder [**wenn SourceDir**](sourcedir.md) nicht in der DefaultDir-Spalte der [Directory-Tabelle](directory-table.md)angegeben ist.

## <a name="example"></a>Beispiel

ICE56 meldet die folgenden Fehler für das gezeigte Beispiel.

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[Verzeichnistabelle](directory-table.md)



| Verzeichnis | \_Übergeordnetes Verzeichnis | DefaultDir |
|-----------|-------------------|------------|
| Targetdir |                   | Temp       |
| Root2     | Root2             | SourceDir  |



 

Um den ersten Fehler zu beheben, sollte der [**TARGETDIR-Stamm**](targetdir.md) den DefaultDir-Wert [**SourceDir**](sourcedir.md)aufweisen. SOURCEDIR wird ebenfalls akzeptiert. Es kann möglich sein, **TARGETDIR** zum übergeordneten Element des zweiten Stamms zu machen und den Wert "." in der DefaultDir-Spalte zu verwenden. Weitere Informationen finden Sie in der [Tabelle Verzeichnis.](directory-table.md)

Um den zweiten Fehler zu beheben, sollte die Verzeichnisstruktur nur über einen Stamm namens [**TARGETDIR**](targetdir.md)verfügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



