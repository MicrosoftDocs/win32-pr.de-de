---
description: Die Tabelle ServiceInstall wird zum Installieren eines Diensts verwendet und weist die folgenden Spalten auf.
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: ServiceInstall-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3850b957df4dd0af662354c14f82717e4b86ad597f151c6a45bb8dc1bebea5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039960"
---
# <a name="serviceinstall-table"></a>ServiceInstall-Tabelle

Die Tabelle ServiceInstall wird zum Installieren eines Diensts verwendet und weist die folgenden Spalten auf.



| Spalte         | Typ                               | Key | Nullwerte zulässig |
|----------------|------------------------------------|-----|----------|
| ServiceInstall | [Identifier](identifier.md)       | J   | N        |
| Name           | [Formatiert](formatted.md)         | N   | N        |
| DisplayName    | [Formatiert](formatted.md)         | N   | J        |
| ServiceType    | [DoubleInteger](doubleinteger.md) | N   | N        |
| StartType      | [DoubleInteger](doubleinteger.md) | N   | N        |
| ErrorControl   | [DoubleInteger](doubleinteger.md) | N   | N        |
| LoadOrderGroup | [Formatiert](formatted.md)         | N   | J        |
| Abhängigkeiten   | [Formatiert](formatted.md)         | N   | J        |
| StartName      | [Formatiert](formatted.md)         | N   | J        |
| Kennwort       | [Formatiert](formatted.md)         | N   | J        |
| Argumente      | [Formatiert](formatted.md)         | N   | J        |
| Komponente\_    | [Identifier](identifier.md)       | N   | N        |
| BESCHREIBUNG    | [Formatiert](formatted.md)         | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>ServiceInstall
</dt> <dd>

Dies ist der Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Diese Spalte ist die Zeichenfolge, die den zu installierende Dienstnamen angibt. Die Zeichenfolge hat eine maximale Länge von 256 Zeichen. Die Dienststeuerungs-Manager-Datenbank behält die Groß-/Kleinschreibung der Zeichen im Dienstnamen bei, bei Vergleichen von Dienstnamen wird jedoch die Groß-/Kleinschreibung nicht beachtet. Schrägstriche (/) und umgekehrter Schrägstrich \\ () sind ungültige Dienstnamenzeichen.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>Displayname
</dt> <dd>

Diese Spalte ist die lokalisierbare Zeichenfolge, die Benutzeroberflächenprogramme zum Identifizieren des Diensts verwenden. Die Zeichenfolge hat eine maximale Länge von 256 Zeichen. Der Dienststeuerungs-Manager behält die Groß-/Kleinschreibung des Anzeigenamens bei, bei Anzeigenamenvergleichen wird jedoch die Groß-/Kleinschreibung nicht beachtet.

</dd> <dt>

<span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>Servicetype
</dt> <dd>

Diese Spalte besteht aus einer Reihe von Bitflags, die den Diensttyp angeben. Einer der folgenden Diensttypen muss in dieser Spalte angegeben werden.



| Diensttyp                | Wert      | BESCHREIBUNG                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SERVICE \_ WIN32 \_ OWN \_ PROCESS   | 0x00000010 | Ein Microsoft Win32-Dienst, der einen eigenen Prozess ausführt.                                                                                                                                                                         |
| \_ \_ DIENST-WIN32-FREIGABEPROZESS \_ | 0x00000020 | Ein Win32-Dienst, der einen Prozess gemeinsam nutzt.                                                                                                                                                                                       |
| \_INTERAKTIVER \_ DIENSTPROZESS  | 0x00000100 | Ein Win32-Dienst, der mit dem Desktop interagiert. Dieser Wert kann nicht allein verwendet werden und muss einem der beiden vorherigen Typen hinzugefügt werden. Die Spalte StartName muss bei Verwendung dieses Flags auf LocalSystem oder NULL festgelegt werden.<br/> |



 

Die folgenden Diensttypen werden nicht unterstützt.



| Diensttyp               | Wert      | BESCHREIBUNG                   |
|-------------------------------|------------|-------------------------------|
| \_ \_ DIENSTKERNELTREIBER       | 0x00000001 | Ein Treiberdienst.             |
| \_ \_ \_ DIENSTDATEISYSTEMTREIBER | 0x00000002 | Ein Dateisystemtreiberdienst. |



 

</dd> <dt>

<span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType
</dt> <dd>

Diese Spalte besteht aus einer Reihe von Bitflags, die angeben, wann der Dienst gestartet werden soll. Einer der folgenden Dienststarttypen muss in dieser Spalte angegeben werden.



| Typ des Dienststarts  | Wert      | BESCHREIBUNG                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| SERVICE \_ AUTO \_ START   | 0x00000002 | Ein Dienst wird während des Systemstarts gestartet.                                                              |
| SERVICE \_ DEMAND \_ START | 0x00000003 | Ein Dienst wird gestartet, wenn der Dienststeuerungs-Manager die [**StartService-Funktion**](/windows/win32/api/winsvc/nf-winsvc-startservicea) aufruft. |
| DIENST \_ DEAKTIVIERT      | 0x00000004 | Gibt einen Dienst an, der nicht mehr gestartet werden kann.                                                         |



 

Der Windows Installer kann die Optionen SERVICE BOOT START und SERVICE SYSTEM START nicht \_ \_ \_ \_ verwenden.

</dd> <dt>

<span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl
</dt> <dd>

Diese Spalte gibt die Aktion an, die vom Startprogramm ausgeführt wird, wenn der Dienst während des Starts nicht gestartet werden kann. Diese Werte wirken sich auf die ServiceControl StartService-Ereignisse für installierte Dienste aus. Eines der folgenden Fehlersteuerungsflags muss in dieser Spalte angegeben werden.

Wenn Sie den Flags in der folgenden Tabelle die Konstante **msidbServiceInstallErrorControlVital** (value = 0x08000) hinzufügen, wird angegeben, dass die Gesamtinstallation fehlschlagen sollte, wenn der Dienst nicht im System installiert werden kann.



| Fehlersteuerungsflag       | Wert      | Aktion des Startprogramms                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DIENSTFEHLER \_ \_ IGNORIEREN   | 0x00000000 | Protokolliert den Fehler und setzt den Startvorgang fort.                                                                                                                                       |
| DIENSTFEHLER \_ \_ NORMAL   | 0x00000001 | Protokolliert den Fehler, zeigt ein Meldungsfeld an und setzt den Startvorgang fort.                                                                                                                    |
| DIENSTFEHLER \_ \_ KRITISCH | 0x00000003 | Protokolliert den Fehler, wenn dies möglich ist und das System mit der letzten als gut bekannten Konfiguration neu gestartet wird. Wenn die letzte als funktionierend bekannte Konfiguration gestartet wird, schlägt der Startvorgang fehl. |



 

</dd> <dt>

<span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup
</dt> <dd>

Diese Spalte enthält die Zeichenfolge, die die Lastreihenfolgegruppe benennt, der dieser Dienst angehört. Geben Sie NULL oder eine leere Zeichenfolge an, wenn der Dienst nicht zu einer Gruppe gehört.

</dd> <dt>

<span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Abhängigkeiten
</dt> <dd>

Diese Spalte enthält eine Liste der Namen von Diensten oder Auslastungsreihenfolgegruppen, die das System vor diesem Dienst starten muss. Trennen Sie Namen in der Liste durch NULL-Werte. Wenn der Dienst über keine Abhängigkeiten verfügt, geben Sie NULL oder eine leere Zeichenfolge an. Verwenden Sie die \[ ~ \] -Syntax, um einen NULL-Wert einzufügen. Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

Um beispielsweise zu verlangen, dass das System service1 und service2 startet, geben Sie service1 service2 in die Spalte Abhängigkeiten ein, bevor der in der Spalte ServiceInstall aufgeführte Dienst gestartet \[ ~ \] \[ ~ \] \[ ~ \] wird. Die Bezeichner service1 und service2 müssen entweder im Primärschlüssel der Tabelle enthalten sein oder der Name des diensts sein, der bereits installiert ist.

Sie müssen Gruppennamen das Präfix + vorangestellt haben, damit sie von einem Dienstnamen unterschieden werden können. Damit das System service1 und mindestens ein Mitglied der Bestellgruppe MyGroup starten muss, bevor der in der Spalte ServiceInstall aufgeführte Dienst gestartet wird, geben Sie service1 \[ ~ \] + MyGroup \[ ~ \] \[ ~ \] ein.

</dd> <dt>

<span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName
</dt> <dd>

Der Dienst wird als name angemeldet, der von der Zeichenfolge in dieser Spalte angegeben wird. Wenn der Diensttyp SERVICE WIN32 OWN PROCESS lautet, \_ verwenden Sie einen \_ \_ Kontonamen im Format DomainName \\ UserName. Wenn das Konto zur integrierten Domäne gehört, ist es zulässig, anzugeben. \\ Nutzername. Das LocalSystem-Konto muss verwendet werden, wenn der Diensttyp SERVICE \_ WIN32 \_ SHARE PROCESS oder SERVICE INTERACTIVE PROCESS \_ \_ \_ lautet. Die [**CreateService-Funktion**](/windows/win32/api/winsvc/nf-winsvc-createservicea) verwendet das LocalSystem-Konto, wenn StartName als NULL angegeben ist und die meisten Dienste diese Spalte daher leer lassen.

</dd> <dt>

<span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>Passwort
</dt> <dd>

Diese Zeichenfolge ist das Kennwort für den Kontonamen, der in der Spalte StartName angegeben ist. Beachten Sie, dass der Benutzer über Berechtigungen zum Anmelden als Dienst verfügen muss. Der Dienst hat kein Kennwort, wenn StartName NULL oder eine leere Zeichenfolge ist. Der Startname von LocalSystem ist NULL, und daher ist das Kennwort in dieser Instanz NULL, sodass die meisten Dienste diese Spalte leer lassen.

Beachten Sie, dass das Installationsprogramm nach dem Löschen eines Diensts, der mit einem Benutzernamen und einem Kennwort installiert wurde, keinen Rollback des Diensts durchführen kann, ohne zuerst eine benutzerdefinierte Aktion zum Abrufen des Kennworts zu verwenden. Das Installationsprogramm kann alle erforderlichen Informationen zum Dienst abrufen, mit Ausnahme des Kennworts, das in einem geschützten Teil des Systems gespeichert ist. Die benutzerdefinierte Aktion erhält das Kennwort, indem der Benutzer dazu aufgefordert wird, eine Eigenschaft aus der Datenbank zu lesen oder eine Datei zu lesen. Die benutzerdefinierte Aktion muss dann [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)aufrufen, um das Kennwort anzugeben, bevor der Dienst neu installiert wird.

Windows Das Installationsprogramm schreibt den in das Feld Kennwort eingegebenen Wert nicht in die Protokolldatei.

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumente
</dt> <dd>

Diese Spalte enthält alle Befehlszeilenargumente oder -eigenschaften, die zum Ausführen des Diensts erforderlich sind.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel zur Spalte einer der [Komponententabellen.](component-table.md) Beachten Sie, dass keyPath für diese Komponente die ausführbare Datei für den Dienst sein muss, um diesen Dienst mithilfe der Tabelle InstallService zu installieren.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Diese Spalte enthält eine lokalisierbare Beschreibung für den dienst, der konfiguriert wird. Wenn diese Spalte leer gelassen wird, verwendet das Installationsprogramm die vorhandene Beschreibung des Diensts, sofern vorhanden. Weitere Informationen finden Sie unter SERVICE \_ DESCRIPTION im Microsoft Windows Software Development Kit (SDK). Geben Sie " " in diese Spalte ein, um eine vorhandene Beschreibung zu \[ ~ \] löschen. Dies führt zu einer leeren Beschreibung für einen neuen oder vorhandenen Dienst.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [InstallServices-Aktion](installservices-action.md) in [*Sequenztabellen*](s-gly.md) verarbeitet die Informationen in dieser Tabelle. Informationen zur Verwendung von *Sequenztabellen* finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

Diese Tabelle enthält die meisten Parameter für die Win32 [**CreateService-Funktion.**](/windows/win32/api/winsvc/nf-winsvc-createservicea)

Obwohl es möglich ist, die Benutzeroberfläche zu verwenden, um anzugeben, dass ein Dienst als "Aus Quelle ausführen" installiert werden soll, unterstützt das Installationsprogramm diese Art der Installation nicht tatsächlich. Dienste, die mit der Berechtigungsstufe des lokalen Systems ausgeführt werden, müssen installiert werden, um von der lokalen Festplatte aus ausgeführt zu werden. Vermeiden Sie die Installation von Diensten, die die Identität der Berechtigungen eines bestimmten Benutzers annehmen, da dies Sicherheitsdaten in ein Protokoll oder die Systemregistrierung schreiben kann. Dies kann möglicherweise zu einem Sicherheitsproblem, einem Kennwortkonflikt oder dem Verlust von Konfigurationsdaten führen, wenn das System neu gestartet wird.

Um einen Dienst während einer Deinstallation zu löschen, muss ein entsprechender Datensatz für den Dienst in der [ServiceControl-Tabelle](servicecontrol-table.md) vorhanden sein, und das **msidbServiceControlEventUninstallDelete-Flag** muss in der Spalte Ereignis angezeigt werden. Das Installationsprogramm löscht einen Dienst in der ServiceInstall-Tabelle während der Deinstallation nicht ohne diesen Eintrag in der ServiceControl-Tabelle.

Informationen zum Sichern eines Diensts finden Sie in der [MsiLockPermissionsEx-Tabelle.](msilockpermissionsex-table.md)

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
