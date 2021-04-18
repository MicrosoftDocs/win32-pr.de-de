---
description: Windows-Verwaltungsinstrumentation (WMI) verfügt über einen neuen Registrierungsschlüssel, um das autorestore-Repository-Feature zu aktivieren oder zu deaktivieren.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Registrierungsschlüssel für die Repository-Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345245"
---
# <a name="registry-key-for-repository-configuration"></a>Registrierungsschlüssel für die Repository-Konfiguration

Windows-Verwaltungsinstrumentation (WMI) verfügt über einen neuen Registrierungsschlüssel, um das autorestore-Repository-Feature zu aktivieren oder zu deaktivieren. Weitere Informationen zum Wiederherstellen des WMI-Repository finden Sie unter [sichern oder Wiederherstellen des WMI-Repository](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).

In Windows 7 ist das Standardverhalten das automatische Wiederherstellen eines Repository aus einer gesicherten Version, wenn eine Repository-Beschädigung erkannt wird. WMI stellt den **autorestoreaktivierten** Registrierungs Wert bereit, um diese Funktion zu deaktivieren.

Die Registrierungsschlüssel für WMI befinden sich in der Registrierung unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

<dl> <dt>

<span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**Autorestoreaktivierte**
</dt> <dd>

Ermöglicht es dem Benutzer, zu bestimmen, ob die autorestore-Repository-Funktion verwendet werden soll. Standardmäßig ist dieser Schlüssel auf 1 festgelegt, und die autorestore-Repository-Funktion ist aktiviert.

Folgende Einstellungen sind möglich:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Disabled

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Aktiviert

</dd> </dl> </dd> </dl>

Der Registrierungs Wert **autorestoreaktivierte** kann mithilfe der Gruppenrichtlinien-Verwaltungskonsole (GPMC) geändert werden. Weitere Informationen finden Sie unter [Gruppenrichtlinien-Verwaltungskonsole](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

Dieses Verfahren enthält Details zum Aktivieren oder Deaktivieren der autorestore-Repository-Funktion:

**So ändern Sie den Standardwert des **autorestoreaktivierten** Schlüssels mithilfe von Gruppenrichtlinie**

1.  Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.
2.  Erstellen Sie ein Gruppenrichtlinie Objekt (GPO).
3.  Bearbeiten Sie das Gruppenrichtlinien Objekt.
4.  Navigieren Sie zu Einstellungen/Windows-Einstellungen/Registrierung.
5.  Klicken Sie mit der rechten Maustaste, und wählen Sie **neu... Registrierung**. Diese Aktion stellt eine Benutzeroberfläche dar, auf der Sie Registrierungsinformationen eingeben können.
6.  Wählen Sie den Befehl **Aktualisieren** aus.
7.  Wählen Sie den folgenden Registrierungsschlüssel Pfad aus: **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WBEM \\ CIMOM**.
8.  Geben Sie im Feld **Name den Namen** **autorestoreaktivierte** ein.
9.  Geben Sie im Feld **Daten** 0 zum Deaktivieren oder 1 ein, um das autorestore-Repository zu aktivieren.
10. Klicken Sie auf OK.

 

 
