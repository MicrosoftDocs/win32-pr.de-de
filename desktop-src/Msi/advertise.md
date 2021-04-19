---
description: Der Wert der Ankündigungs Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind, die angekündigt werden sollen.
ms.assetid: ef97f70b-e4bf-4eb3-b643-046a9c348823
title: Ankündigungs Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e768f22f86dacf35009ca0e0e3ef9337ef84ab70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367697"
---
# <a name="advertise-property"></a>Ankündigungs Eigenschaft

Der **Wert der Ankündigungs Eigenschaft ist** eine Liste von Funktionen, die durch Kommas getrennt sind, die angekündigt werden sollen. Die Funktionen müssen in der featurespalte der [Funktions](feature-table.md) Tabelle vorhanden sein. Wenn Sie alle Features wie angekündigt installieren möchten, verwenden Sie Ankündigungs = alle in der Befehlszeile. Geben Sie ankündigen = all nicht in die [Eigenschaften Tabelle](property-table.md) ein, da dadurch ein angekündigtes Paket generiert wird, das nicht installiert oder entfernt werden kann.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass bei Funktionsnamen die Groß-/Kleinschreibung beachtet

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Aufgeh**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**Adddefault**](adddefault.md)
5.  [**Installieren Sie**](reinstall.md)
6.  **Benen**
7.  [**Compaddlocal**](compaddlocal.md)
8.  [**Compaddsource**](compaddsource.md)
9.  [**Compadddefault**](compadddefault.md)
10. [**Fileaddlocal**](fileaddlocal.md)
11. [**Fileaddsource**](fileaddsource.md)
12. [**Fileadddefault**](fileadddefault.md)

Wenn die Befehlszeile z. b. Folgendes angibt: ADDLOCAL = ALL, addsource = myfeature, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt. Wenn die Befehlszeile "ADDSOURCE = ALL", "ADDLOCAL = myfeature" lautet, ist "First myfeature" auf "Run-local" festgelegt, und wenn "ADDSOURCE = ALL" ausgewertet wird, werden alle Funktionen (einschließlich "myfeature") auf "Run-From-Source" zurückgesetzt.

Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




