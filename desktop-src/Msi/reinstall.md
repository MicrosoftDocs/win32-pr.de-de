---
description: Der Wert der Eigenschaft neu installieren ist eine Liste von Funktionen, die durch Kommas getrennt sind, die neu installiert werden sollen. Die aufgeführten Features müssen in der featurespalte der Funktions Tabelle vorhanden sein. Verwenden Sie zum erneuten Installieren aller Features installieren Sie = all in der Befehlszeile.
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: Eigenschaft neu installieren
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357694"
---
# <a name="reinstall-property"></a>Eigenschaft neu installieren

Der Wert der Eigenschaft **neu installieren** ist eine Liste von Funktionen, die durch Kommas getrennt sind, die neu installiert werden sollen. Die aufgeführten Features müssen in der featurespalte der [Funktions](feature-table.md) Tabelle vorhanden sein. Verwenden Sie zum erneuten Installieren aller Features installieren Sie = all in der Befehlszeile.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass die Funktionsnamen die Groß-/Kleinschreibung beachten.

Wenn die Eigenschaft **neu installieren** festgelegt ist, sollte auch die Eigenschaft [**REINSTALLMODE**](reinstallmode.md) festgelegt werden, um die Art der erneuten Installation anzugeben, die ausgeführt werden soll. Wenn die Eigenschaft **REINSTALLMODE** nicht festgelegt ist, werden standardmäßig alle Dateien, die derzeit installiert sind, neu installiert, wenn die aktuell installierte Datei eine geringere Version (oder nicht vorhanden) ist. Standardmäßig werden keine Registrierungseinträge umgeschrieben.

Beachten Sie, dass auch dann, wenn die **Neuinstallation** auf alle festgelegt ist, nur die Features, die bereits zuvor installiert waren, neu installiert werden. Wenn für ein Produkt, das noch installiert werden soll, die **Neuinstallation** festgelegt ist, wird daher überhaupt keine Installations Aktion durchgeführt.

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Aufgeh**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**Adddefault**](adddefault.md)
5.  **Installieren Sie**
6.  [**Benen**](advertise.md)
7.  [**Compaddlocal**](compaddlocal.md)
8.  [**Compaddsource**](compaddsource.md)
9.  [**Fileaddlocal**](fileaddlocal.md)
10. [**Fileaddsource**](fileaddsource.md)
11. [**Fileadddefault**](fileadddefault.md)

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

 

 




