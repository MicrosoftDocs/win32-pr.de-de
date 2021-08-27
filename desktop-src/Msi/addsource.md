---
description: Der Wert der ADDSOURCE-Eigenschaft ist eine Liste von Features, die durch Kommas getrennt sind und installiert werden müssen, um von der Quelle aus ausgeführt zu werden.
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: ADDSOURCE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420ca53a96ddeb379a7e021db2c45157861acfb62d066cadfc7a163db7fbc307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078160"
---
# <a name="addsource-property"></a>ADDSOURCE-Eigenschaft

Der Wert der **ADDSOURCE-Eigenschaft** ist eine Liste von Features, die durch Kommas getrennt sind und installiert werden müssen, um von der Quelle aus ausgeführt zu werden. Die Features müssen in der Spalte Feature der [Featuretabelle](feature-table.md)vorhanden sein. Verwenden Sie ADDSOURCE=ALL in der Befehlszeile, um alle Funktionen während der Ausführung aus der Quelle zu installieren. Geben Sie ADDSOURCE=ALL nicht in die [Eigenschaftentabelle](property-table.md)ein, da dadurch ein Aus-Quell-Paket generiert wird, das nicht ordnungsgemäß entfernt werden kann.

## <a name="remarks"></a>Hinweise

Bei den Featurenamen wird die Groß-/Kleinschreibung beachtet. Wenn das LocalOnly-Bitflag in der Spalte Attribute der [Komponententabelle](component-table.md) für eine Komponente eines Features in der Liste festgelegt ist, wird diese Komponente installiert, um lokal ausgeführt zu werden.

Das Installationsprogramm wertet immer die folgenden Eigenschaften in der folgenden Reihenfolge aus:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Entfernen**](remove.md)
3.  **ADDSOURCE**
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Installieren**](reinstall.md)
6.  [**Werben**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Beispiel:

-   Wenn in der Befehlszeile Folgendes angegeben ist: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, werden alle Features zuerst auf "run-local" und dann auf **"MyFeature"** auf "run-from-source" festgelegt.
-   Wenn die Befehlszeile lautet: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, wird **zuerst MyFeature** auf run-local festgelegt, und wenn ADDSOURCE=ALL ausgewertet wird, werden alle Features (einschließlich **MyFeature**) auf run-from-source zurückgesetzt.

Das Installationsprogramm legt die [**Vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation oder wenn eine der oben genannten Eigenschaften in der Befehlszeile angegeben wird, auf den Wert "1" fest.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




