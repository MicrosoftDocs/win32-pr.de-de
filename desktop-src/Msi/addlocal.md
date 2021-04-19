---
description: Der Wert der ADDLOCAL-Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind und lokal installiert werden sollen.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: ADDLOCAL (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9618389d6e409829dce1eb7bb3a38c1269a2e06d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372761"
---
# <a name="addlocal-property"></a>ADDLOCAL (Eigenschaft)

Der Wert der **ADDLOCAL** -Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind und lokal installiert werden sollen. Die Funktionen müssen in der featurespalte der [Funktions Tabelle](feature-table.md)vorhanden sein. Wenn Sie alle Features lokal installieren möchten, verwenden Sie ADDLOCAL = all in der Befehlszeile. Geben Sie ADDLOCAL = ALL nicht in die [Eigenschaften Tabelle](property-table.md)ein, da dadurch ein lokal installiertes Paket generiert wird, das nicht ordnungsgemäß entfernt werden kann.

## <a name="remarks"></a>Bemerkungen

Bei Funktionsnamen wird die Groß-/Kleinschreibung Wenn das sourceOnly-Bitflag in der Spalte Attribute der [Komponenten Tabelle](component-table.md) für eine Komponente eines Features in der Liste festgelegt ist, wird diese Komponente als aus Quelle ausgeführt installiert.

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:

1.  **ADDLOCAL**
2.  [**Aufgeh**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**Adddefault**](adddefault.md)
5.  [**Installieren Sie**](reinstall.md)
6.  [**Benen**](advertise.md)
7.  [**Compaddlocal**](compaddlocal.md)
8.  [**Compaddsource**](compaddsource.md)
9.  [**Compadddefault**](compadddefault.md)
10. [**Fileaddlocal**](fileaddlocal.md)
11. [**Fileaddsource**](fileaddsource.md)
12. [**Fileadddefault**](fileadddefault.md)

Beispiel:

-   Wenn in der Befehlszeile Folgendes angegeben wird: ADDLOCAL = ALL, addsource = **myfeature**, werden alle Features zuerst auf Run-Local festgelegt, und **myfeature** wird auf Run-From-Source festgelegt.
-   Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL =**myfeature**" lautet, ist "First **myfeature** " auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich " **myfeature**") auf "Run-From-Source" zurückgesetzt.

Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der vorherigen Eigenschaften in der Befehlszeile angegeben wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




