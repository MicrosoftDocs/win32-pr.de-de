---
description: Der Wert der COMPADDSOURCE-Eigenschaft ist eine Liste von Komponenten-GUIDs aus der ComponentId -Spalte der Component-Tabelle, getrennt durch Kommas, die für die Ausführung auf dem Quellmedium installiert werden sollen.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: COMPADDSOURCE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f68e795a9092892212f41a073a8e5a80945f57be14224e576262c30bba92707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380052"
---
# <a name="compaddsource-property"></a>COMPADDSOURCE-Eigenschaft

Der Wert der **COMPADDSOURCE-Eigenschaft** ist eine Liste von Komponenten-GUIDs aus der ComponentId -Spalte der Component-Tabelle, getrennt durch Kommas, die für die Ausführung auf dem Quellmedium installiert werden sollen. [](component-table.md) Das Installationsprogramm verwendet diesen Wert, um basierend auf den angegebenen Komponenten zu bestimmen, welche Funktionen zur Ausführung aus der Quelle installiert werden sollen. Für jede aufgeführte Komponenten-ID überprüft das Installationsprogramm alle Funktionen, die (über die [Tabelle FeatureComponents)](featurecomponents-table.md) mit dieser Komponente verknüpft sind, und installiert das Feature, das die geringste Menge an Speicherplatz für die Installation erfordert. Die aufgelisteten Komponenten müssen in der Spalte Komponente der Tabelle [Komponente vorhanden](component-table.md) sein.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass bei den Komponentennamen die Schreibung beachtet wird. Beachten Sie außerdem Folgendes: Wenn das LocalOnly-Bitflag in der Spalte Attribute der Component-Tabelle für eine Komponente festgelegt ist, wird die Komponente für die lokale Ausführung installiert. [](component-table.md)

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Entfernen**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Installieren**](reinstall.md)
6.  [**Werben**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  **COMPADDSOURCE**
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Wenn die Befehlszeile z. B. FOLGENDEs angibt: ADDLOCAL=ALL, ADDSOURCE = MyFeature, werden alle Features zuerst auf run-local und dann myFeature auf run-from-source festgelegt. Wenn die Befehlszeile auf ADDSOURCE=ALL, ADDLOCAL=MyFeature festgelegt ist, wird zuerst MyFeature auf run-local festgelegt, und wenn ADDSOURCE=ALL ausgewertet wird, werden alle Features (einschließlich MyFeature) auf die Ausführung aus der Quelle zurückgesetzt.

Das Installationsprogramm legt die [**Preselected-Eigenschaft**](preselected.md) während der Wiederaufnahme einer angehaltenen Installation oder bei Angabe einer der oben genannten Eigenschaften in der Befehlszeile auf den Wert "1" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




