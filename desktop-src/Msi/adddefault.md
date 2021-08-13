---
description: Der Wert der ADDDEFAULT-Eigenschaft ist eine Liste von Features, die durch Kommas getrennt sind und in ihrer Standardkonfiguration installiert werden sollen.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: ADDDEFAULT-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e854df38b58a19f41f98cf1f96657dafdda0c4134c7085c50b4c9c4528b3164e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639704"
---
# <a name="adddefault-property"></a>ADDDEFAULT-Eigenschaft

Der Wert der **ADDDEFAULT-Eigenschaft** ist eine Liste von Features, die durch Kommas getrennt sind und in ihrer Standardkonfiguration installiert werden sollen. Die Features müssen in der Spalte Feature der [Featuretabelle vorhanden sein.](feature-table.md) Um alle Features in ihren Standardkonfigurationen zu installieren, verwenden Sie ADDDEFAULT=ALL in der Befehlszeile.

Ein in der **ADDDEFAULT-Eigenschaft** aufgeführtes Feature wird im gleichen Installationszustand installiert, als ob der Benutzer eine Bedarfsbasierte Installation des Features angefordert hätte. Der Zustand wird durch die Bits bestimmt, die für das Feature in der Spalte Attribute der [Featuretabelle](feature-table.md)festgelegt sind, und welche Bits für die Featurekomponenten in der Spalte Attribute der [Komponententabelle festgelegt werden.](component-table.md)

## <a name="remarks"></a>Hinweise

Bei den Featurenamen wird die Kleinschreibung beachtet.

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Entfernen**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  **ADDDEFAULT**
5.  [**Installieren**](reinstall.md)
6.  [**Werben**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Beispiel:

-   Wenn die Befehlszeile angibt: ADDLOCAL=ALL, ADDSOURCE = MyFeature, werden alle Features zuerst auf run-local und dann **myFeature** auf run-from-source festgelegt.
-   Wenn die Befehlszeile auf ADDSOURCE=ALL, ADDLOCAL=MyFeature festgelegt ist, wird zuerst **MyFeature** auf run-local festgelegt, und wenn ADDSOURCE=ALL ausgewertet wird, werden alle Features (einschließlich **MyFeature)** auf die Ausführung aus der Quelle zurückgesetzt.

Das Installationsprogramm legt die [**Preselected-Eigenschaft**](preselected.md) während der Wiederaufnahme einer angehaltenen Installation oder bei Angabe einer der oben genannten Eigenschaften in der Befehlszeile auf den Wert "1" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Requirements (Anforderungen für den Windows Installer).<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




