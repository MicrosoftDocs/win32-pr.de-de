---
description: Die servicabstall-Tabelle wird verwendet, um einen Dienst zu installieren, der über die folgenden Spalten verfügt.
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: Servicabstall-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502583802a26c10bfd9572375149720c7c597f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358565"
---
# <a name="serviceinstall-table"></a>Servicabstall-Tabelle

Die servicabstall-Tabelle wird verwendet, um einen Dienst zu installieren, der über die folgenden Spalten verfügt.



| Spalte         | Typ                               | Schlüssel | Nullwerte zulässig |
|----------------|------------------------------------|-----|----------|
| Serviceingestall | [Bezeichner](identifier.md)       | J   | N        |
| Name           | [Großformatige](formatted.md)         | N   | N        |
| DisplayName    | [Großformatige](formatted.md)         | N   | J        |
| ServiceType    | [Doubleiteger](doubleinteger.md) | N   | N        |
| StartType      | [Doubleiteger](doubleinteger.md) | N   | N        |
| ErrorControl   | [Doubleiteger](doubleinteger.md) | N   | N        |
| LoadOrderGroup | [Großformatige](formatted.md)         | N   | J        |
| Abhängigkeiten   | [Großformatige](formatted.md)         | N   | J        |
| StartName      | [Großformatige](formatted.md)         | N   | J        |
| Kennwort       | [Großformatige](formatted.md)         | N   | J        |
| Argumente      | [Großformatige](formatted.md)         | N   | J        |
| Komponente\_    | [Bezeichner](identifier.md)       | N   | N        |
| BESCHREIBUNG    | [Großformatige](formatted.md)         | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>Serviceingestall
</dt> <dd>

Dies ist der Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Diese Spalte ist die Zeichenfolge, mit der der zu installier End Dienst Name erteilt wird. Die Zeichenfolge hat eine maximale Länge von 256 Zeichen. Die Dienststeuerungs-Manager-Datenbank behält die Groß-/Kleinschreibung der Zeichen im Dienstnamen bei Ein Schrägstrich (/) und ein umgekehrter Schrägstrich ( \\ ) sind ungültige Dienst namens Zeichen.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>Display Name
</dt> <dd>

Diese Spalte ist die lokalisierbare Zeichenfolge, mit der Benutzeroberflächen Programme den Dienst identifizieren. Die Zeichenfolge hat eine maximale Länge von 256 Zeichen. Der Dienststeuerungs-Manager behält die Groß-/Kleinschreibung des anzeigen Amens bei

</dd> <dt>

<span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>Service Type
</dt> <dd>

Bei dieser Spalte handelt es sich um einen Satz von Bitflags, die den Diensttyp angeben. In dieser Spalte muss einer der folgenden Dienst Typen angegeben werden.



| Diensttyp                | Wert      | BESCHREIBUNG                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Eigener Win32-Dienst \_ \_ Prozess   | 0x00000010 | Ein Microsoft Win32-Dienst, der seinen eigenen Prozess ausführt.                                                                                                                                                                         |
| \_Win32- \_ Freigabe \_ Prozess für Dienst | 0x00000020 | Ein Win32-Dienst, der einen Prozess freigibt.                                                                                                                                                                                       |
| \_interaktiver Dienst \_ Prozess  | 0x00000100 | Ein Win32-Dienst, der mit dem Desktop interagiert. Dieser Wert kann nicht allein verwendet werden und muss einem der beiden vorherigen Typen hinzugefügt werden. Bei Verwendung dieses Flags muss die StartName-Spalte auf LocalSystem oder NULL festgelegt werden.<br/> |



 

Die folgenden Dienst Typen werden nicht unterstützt.



| Diensttyp               | Wert      | BESCHREIBUNG                   |
|-------------------------------|------------|-------------------------------|
| Dienst \_ -Kernel- \_ Treiber       | 0x00000001 | Ein Treiber Dienst.             |
| Dienst \_ Datei \_ System- \_ Treiber | 0x00000002 | Ein Dateisystem-Treiber Dienst. |



 

</dd> <dt>

<span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType
</dt> <dd>

Bei dieser Spalte handelt es sich um einen Satz von Bitflags, die angeben, wann der Dienst gestartet werden soll. In dieser Spalte muss einer der folgenden Typen von Dienst Starts angegeben werden.



| Typ des Dienst Starts  | Wert      | BESCHREIBUNG                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| \_automatischer Dienst \_ Start   | 0x00000002 | Ein Dienst wird beim Systemstart gestartet.                                                              |
| Service \_ Demand- \_ Start | 0x00000003 | Ein Dienst wird gestartet, wenn der Dienststeuerungs-Manager die [**Start Service**](/windows/win32/api/winsvc/nf-winsvc-startservicea) -Funktion aufruft. |
| Dienst \_ deaktiviert      | 0x00000004 | Gibt einen Dienst an, der nicht mehr gestartet werden kann.                                                         |



 

Der Windows Installer kann die Startoptionen für Dienst Starts \_ \_ und Dienst System nicht verwenden \_ \_ .

</dd> <dt>

<span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl
</dt> <dd>

Diese Spalte gibt die vom Start Programm ausgeführte Aktion an, wenn der Dienst beim Start nicht gestartet werden kann. Diese Werte wirken sich auf die ServiceControl-StartService-Ereignisse für installierte Dienste aus. In dieser Spalte muss eines der folgenden fehlersteuerungflags angegeben werden.

Durch das Hinzufügen der Konstanten **msidbserviceinstallerrorcontrolvital** (Value = 0x08000) zu den Flags in der folgenden Tabelle wird angegeben, dass die allgemeine Installation fehlschlagen soll, wenn der Dienst nicht im System installiert werden kann.



| Fehlersteuerungsflag       | Wert      | Aktion des Start Programms                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dienst \_ Fehler \_ ignorieren   | 0x00000000 | Protokolliert den Fehler und setzt den Startvorgang fort.                                                                                                                                       |
| Dienst \_ Fehler \_ Normal   | 0x00000001 | Protokolliert den Fehler, zeigt ein Meldungs Feld an und setzt den Startvorgang fort.                                                                                                                    |
| Dienst \_ Fehler \_ kritisch | 0x00000003 | Protokolliert den Fehler, falls dies möglich ist, und das System wird neu gestartet, und die letzte Konfiguration ist gut bekannt. Wenn die zuletzt bekannte, gute Konfiguration gestartet wird, tritt beim Startvorgang ein Fehler auf. |



 

</dd> <dt>

<span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup
</dt> <dd>

Diese Spalte enthält die Zeichenfolge, die die Gruppe der Lade Reihen benennt, in der dieser Dienst Mitglied ist. Geben Sie NULL oder eine leere Zeichenfolge an, wenn der Dienst nicht zu einer Gruppe gehört.

</dd> <dt>

<span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Zen
</dt> <dd>

Diese Spalte ist eine Liste der Namen von Diensten oder lade Auftrags Gruppen, die das System vor diesem Dienst starten muss. Trennen Sie die Namen in der Liste durch Nullen. Wenn der Dienst keine Abhängigkeiten aufweist, geben Sie NULL oder eine leere Zeichenfolge an. Verwenden Sie die Syntax \[ ~ \] , um einen NULL-Wert einzufügen. Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

Um z. b. festzulegen, dass das System Service1 und Service2 starten muss, bevor der Dienst in der ServiceInstall-Spalte aufgeführt wird, geben Sie Service1 \[ ~ \] Service2 \[ ~ \] \[ ~ \] in die Spalte Abhängigkeiten ein. Die Bezeichner Service1 und Service2 müssen entweder im Primärschlüssel der Tabelle oder im Namen des bereits installierten Dienstanbieter vorkommen.

Sie müssen Gruppennamen mit + als Präfix versehen, damit Sie von einem Dienstnamen unterschieden werden können. Geben Sie Service1 \[ ~ \] + myGroup ein, \[ ~ \] \[ um ~ \] zu verlangen, dass das System Service1 und mindestens ein Mitglied der Bestell Gruppe myGroup startet, bevor Sie den Dienst in der ServiceInstall-Spalte auflisten.

</dd> <dt>

<span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName
</dt> <dd>

Der Dienst ist als der von der Zeichenfolge in dieser Spalte angegebene Name angemeldet. Wenn der Diensttyp der Dienst \_ Win32-Prozess ist, \_ verwenden Sie \_ einen Kontonamen im Format Domain Name \\ username. Wenn das Konto zur integrierten Domäne gehört, dürfen Sie angeben. \\ User. Das LocalSystem-Konto muss verwendet werden, wenn der Diensttyp ein \_ Win32- \_ Freigabe \_ Prozess oder Dienst \_ interaktiver Prozess ist \_ . Die Funktion "{ [**ateservice**](/windows/win32/api/winsvc/nf-winsvc-createservicea) " verwendet das LocalSystem-Konto, wenn "StartName" als NULL angegeben ist und die meisten Dienste daher diese Spalte leer lassen.

</dd> <dt>

<span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>Anmelden
</dt> <dd>

Diese Zeichenfolge ist das Kennwort für den Kontonamen, der in der StartName-Spalte angegeben ist. Beachten Sie, dass der Benutzer über Berechtigungen zum Anmelden als Dienst verfügen muss. Der Dienst hat kein Kennwort, wenn StartName NULL oder eine leere Zeichenfolge ist. Der StartName von "LocalSystem" ist NULL, und das Kennwort in dieser Instanz ist daher NULL, sodass die meisten Dienste diese Spalte leer lassen.

Beachten Sie, dass das Installationsprogramm nach dem Löschen eines Dienstes, der mit einem Benutzernamen und einem Kennwort installiert wurde, kein Rollback für den Dienst ausführen kann, ohne zuvor eine benutzerdefinierte Aktion zum erhalten des Kennworts Das Installationsprogramm kann alle erforderlichen Informationen zum Dienst abrufen, mit Ausnahme des Kennworts, das in einem geschützten Teil des Systems gespeichert wird. Die benutzerdefinierte Aktion erhält das Kennwort, indem der Benutzer dazu aufgefordert wird, eine Eigenschaft aus der Datenbank zu lesen oder eine Datei zu lesen. Die benutzerdefinierte Aktion muss dann [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)aufzurufen, um das Kennwort bereitzustellen, bevor der Dienst neu installiert wird.

Der in das Kenn Wortfeld eingegebene Wert wird von Windows Installer nicht in die Protokolldatei geschrieben.

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentation
</dt> <dd>

Diese Spalte enthält alle Befehlszeilenargumente oder-Eigenschaften, die zum Ausführen des Dienstanbieter erforderlich sind.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel für Spalte einer der [Komponenten Tabellen](component-table.md). Beachten Sie, dass der KEYPATH für diese Komponente die ausführbare Datei für den Dienst sein muss, um diesen Dienst mithilfe der installservice-Tabelle zu installieren.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Diese Spalte enthält eine lokalisierbare Beschreibung für den konfigurierten Dienst. Wenn diese Spalte leer bleibt, verwendet das Installationsprogramm die vorhandene Beschreibung des Dienstanbieter, sofern vorhanden. Weitere Informationen finden Sie unter Dienst \_ Beschreibung im Microsoft Windows Software Development Kit (SDK). Geben Sie zum Löschen einer vorhandenen Beschreibung \[ ~ \] in dieser Spalte "" ein. Dies führt zu einer leeren Beschreibung für einen neuen oder vorhandenen Dienst.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [installservices](installservices-action.md) -Aktion in [*Sequenz Tabellen*](s-gly.md) verarbeitet die Informationen in dieser Tabelle. Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

Diese Tabelle hat die meisten Parameter für die Win32-Funktion " [**deeservice**](/windows/win32/api/winsvc/nf-winsvc-createservicea) ".

Obwohl es möglich ist, die Benutzeroberfläche zu verwenden, um anzugeben, dass ein Dienst als aus der Quelle ausführbare Version installiert werden soll, wird diese Art der Installation vom Installationsprogramm nicht unterstützt. Dienste, die mit der Berechtigungsstufe des lokalen Systems ausgeführt werden, müssen installiert sein, um von der lokalen Festplatte ausgeführt werden zu können. Vermeiden Sie die Installation von Diensten, die die Berechtigungen eines bestimmten Benutzers annehmen, da dadurch Sicherheitsdaten in ein Protokoll oder die Systemregistrierung geschrieben werden können. Dies kann potenziell zu einem Sicherheitsproblem, einem Kenn Wort Konflikt oder dem Verlust von Konfigurationsdaten führen, wenn das System neu gestartet wird.

Um einen Dienst während einer Neuinstallation zu löschen, muss ein entsprechender Datensatz für den Dienst in der [Tabelle ServiceControl](servicecontrol-table.md) vorhanden sein, und das Flag **msidbservicecontroleventuninstalldelete** muss in der Spalte Ereignis angezeigt werden. Der Installer löscht in der Tabelle ServiceInstall während der deinstalstallation keinen Dienst, ohne diesen Eintrag in der Tabelle ServiceControl zu verwenden.

Informationen zum Sichern eines dienstanzdienstanbieter finden Sie in der [Tabelle "msilockpermissionsex](msilockpermissionsex-table.md)".

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
