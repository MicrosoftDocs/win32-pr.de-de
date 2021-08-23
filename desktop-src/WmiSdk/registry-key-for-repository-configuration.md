---
description: Windows Die Verwaltungsinstrumentation (Management Instrumentation, WMI) verfügt über einen neuen Registrierungsschlüssel zum Aktivieren oder Deaktivieren der AutoRestore-Repositoryfunktion.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Registrierungsschlüssel für die Repositorykonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5096945d89fb56fe62de4d5dbda9545f242992e9ae1382723a95792c9500c016
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992450"
---
# <a name="registry-key-for-repository-configuration"></a>Registrierungsschlüssel für die Repositorykonfiguration

Windows Die Verwaltungsinstrumentation (Management Instrumentation, WMI) verfügt über einen neuen Registrierungsschlüssel zum Aktivieren oder Deaktivieren der AutoRestore-Repositoryfunktion. Weitere Informationen zum Wiederherstellen des WMI-Repositorys finden Sie unter Sichern oder Wiederherstellen des [WMI-Repositorys.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11))

In Windows 7 besteht das Standardverhalten darin, ein Repository automatisch aus einer gesicherten Version wiederherzustellen, wenn eine Repositorybeschädigung erkannt wird. WMI stellt den Registrierungswert **AutoRestoreEnabled** bereit, um dieses Feature zu deaktivieren.

Die Registrierungsschlüssel für WMI befinden sich in der Registrierung unter **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

<dl> <dt>

<span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**
</dt> <dd>

Ermöglicht dem Benutzer, zu bestimmen, ob das AutoRestore-Repositoryfeature verwendet werden soll. Dieser Schlüssel ist standardmäßig auf 1 festgelegt, und das Feature AutoRestore-Repository ist aktiviert.

Die folgenden Einstellungen sind möglich:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Disabled

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Aktiviert

</dd> </dl> </dd> </dl>

Der **Registrierungswert AutoRestoreEnabled** kann mithilfe des Gruppenrichtlinien-Verwaltungskonsole (GPMC) geändert werden. Weitere Informationen finden Sie unter [Gruppenrichtlinien-Verwaltungskonsole](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

Dieses Verfahren enthält Details zum Aktivieren oder Deaktivieren des AutoRestore-Repositoryfeatures:

**So ändern Sie den Standardwert des **AutoRestoreEnabled-Schlüssels** mithilfe von Gruppenrichtlinie**

1.  Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.
2.  Erstellen Sie ein Gruppenrichtlinie-Objekt (GPO).
3.  Bearbeiten Sie das Gruppenrichtlinienobjekt.
4.  Navigieren Sie zu Einstellungen/Windows Einstellungen/Registrierung.
5.  Klicken Sie mit der rechten Maustaste, und wählen Sie **Neu... aus. Registrierung**. Diese Aktion stellt eine Benutzeroberfläche dar, auf der Sie Registrierungsinformationen eingeben können.
6.  Wählen Sie den Befehl **Aktualisieren** aus.
7.  Wählen Sie den folgenden Registrierungsschlüsselpfad aus: **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ WBEM \\ CIMOM**.
8.  Geben Sie im **Feld Name** **autoRestoreEnabled** ein.
9.  Geben Sie im **Datenfeld** 0 ein, um es zu deaktivieren, oder 1, um das Feature AutoRestore-Repository zu aktivieren.
10. Klicken Sie auf OK.

 

 
