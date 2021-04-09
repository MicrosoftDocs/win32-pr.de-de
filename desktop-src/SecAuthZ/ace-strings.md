---
description: Erläutert die Zeichen folgen, die in einem Zugriffs Steuerungs Eintrag verwendet werden.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: ACE-Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a35bde18a1ca3ac416faa42e3b693e26305beb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756185"
---
# <a name="ace-strings"></a>ACE-Zeichen folgen

Die [Security Deskriptor Definition Language](security-descriptor-definition-language.md) (SDDL) verwendet ACE-Zeichen folgen in den DACL-und SACL-Komponenten einer [*sicherheitsbeschreibungerzeichenfolge*](/windows/desktop/SecGloss/s-gly) .

Wie in den Beispielen für das [Format der Sicherheits Deskriptor-Zeichen](security-descriptor-string-format.md) Folge gezeigt, wird jeder ACE in einer sicherheitsbeschreibungerzeichenfolge in Klammern eingeschlossen. Die Felder des ACE liegen in der folgenden Reihenfolge vor und sind durch Semikolons (;) getrennt.

> [!Note]  
> Es gibt ein anderes Format für bedingte [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) als andere ACE-Typen. Informationen zu bedingten ACEs finden Sie unter [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a>Felder

<dl> <dt>

<span id="ace_type"></span><span id="ACE_TYPE"></span>**ACE- \_ Typ**
</dt> <dd>

Eine Zeichenfolge, die den Wert des **AceType** -Members der [**ACE- \_ Header**](/windows/desktop/api/Winnt/ns-winnt-ace_header) Struktur angibt. Die ACE-Typzeichenfolge kann eine der folgenden Zeichen folgen sein, die in SDDL. h definiert sind.



| ACE-Zeichenfolge | Konstante in SDDL. h                      | AceType-Wert                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| „A“             | SDDL- \_ Zugriff \_ zulässig                   | Zugriffs zulässiger \_ \_ ACE- \_ Typ                                                                                                                                         |
| "D"             | SDDL- \_ Zugriff \_ verweigert                    | ACE-Typ "Zugriff \_ verweigert" \_ \_                                                                                                                                          |
| OA            | SDDL- \_ Objekt \_ Zugriff \_ zulässig           | Zugriffs zulässiger \_ \_ Objekt-ACE- \_ \_ Typ                                                                                                                                 |
| Gen            | SDDL- \_ Objekt \_ Zugriff \_ verweigert            | Zugriffs \_ Verweigerungs \_ Objekt- \_ ACE- \_ Typ                                                                                                                                  |
| Thaus            | SDDL \_ -Überwachung                             | Systemüberwachungs- \_ \_ ACE- \_ Typ                                                                                                                                           |
| Irdische            | SDDL- \_ Alarm                             | Systemalarm- \_ \_ ACE- \_ Typ                                                                                                                                           |
| Klägerin            | SDDL- \_ Objektüberwachung \_                     | Systemüberwachungs \_ \_ Objekt-ACE- \_ \_ Typ                                                                                                                                   |
| Übernachten            | SDDL- \_ Objekt \_ Alarm                     | \_Systemalarm \_ - \_ Objekttyp \_                                                                                                                                   |
| 150            | erforderliche SDDL- \_ \_ Bezeichnung                  | \_systemobligatorischer \_ Bezeichnung \_ ACE- \_ Typ                                                                                                                                |
| Geleitet            | SDDL- \_ Rückruf \_ Zugriff \_ zulässig         | Zugriffs zulässiger \_ \_ Rückruf \_ \_ -ACE **-Typ Windows Vista und Windows Server 2003:** nicht verfügbar.<br/>                                                           |
| XD            | SDDL- \_ Rückruf \_ Zugriff \_ verweigert          | \_Rückruf-Rückruf für den Zugriff verweigert \_ \_ \_ **: Windows Vista und Windows Server 2003:** nicht verfügbar.<br/>                                                            |
| RA            | SDDL- \_ Ressourcen \_ Attribut               | System \_ Ressourcen \_ Attribut- \_ ACE- \_ Typ **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** nicht verfügbar.<br/> |
| El            | SDDL-Bereichs bezogene \_ \_ Richtlinien- \_ ID                | System weite \_ \_ Richtlinien- \_ ID \_ ACE \_ Type **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** nicht verfügbar.<br/>  |
| Distrikt            | SDDL- \_ Rückruf Überwachung \_                   | \_ \_ Rückruf-ACE für System Überwachung \_ \_ **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** nicht verfügbar.<br/>     |
| D            | SDDL- \_ Rückruf \_ Objekt \_ Zugriff \_ zulässig | Zugriffs zulässiger \_ \_ Rückruf \_ -ACE- \_ Typ **: Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** nicht verfügbar.<br/>   |



 

> [!Note]  
> Wenn der **ACE- \_ Typ** Access \_ Allowed \_ Object \_ \_ -ACE-Typ ist und weder für die **Objekt- \_ GUID** noch für die **Vererbungs \_ Objekt- \_ GUID** eine [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) angegeben ist, konvertiert [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) den **ACE- \_ Typ** in den \_ zulässigen ACE- \_ \_ Typ.

 

</dd> <dt>

<span id="ace_flags"></span><span id="ACE_FLAGS"></span>**ACE- \_ Flags**
</dt> <dd>

Eine Zeichenfolge, die den Wert des **AceFlags** -Members der [**ACE- \_ Header**](/windows/desktop/api/Winnt/ns-winnt-ace_header) Struktur angibt. Die ACE-Flags-Zeichenfolge kann eine Verkettung der folgenden Zeichen folgen sein, die in SDDL. h definiert sind.



| ACE Flags-Zeichenfolge | Konstante in SDDL. h       | Aceflag-Wert                 |
|------------------|--------------------------|-------------------------------|
| RKI             | SDDL- \_ Container \_ erben | Container \_ erben ( \_ ACE)       |
| Zählen             | SDDL- \_ Objekt \_ erben    | Objekt \_ erben ( \_ ACE)          |
| Ecken             | SDDL \_ nicht weitergegeben \_      | kein \_ propagieren- \_ \_ ACE erben   |
| Brasilianer             | nur SDDL \_ erben \_      | \_nur \_ ACE erben            |
| „ID“             | SDDL \_ geerbt          | geerbte \_ ACE                |
| SAS             | SDDL-Überwachung \_ \_ erfolgreich     | RAS-Flag für erfolgreiches \_ zugreifen \_ \_ |
| Übergangs             | Fehler bei SDDL-Überwachung. \_ \_     | fehlerhafter \_ Access- \_ ACE- \_ Flag     |



 

</dd> <dt>

<span id="rights"></span><span id="RIGHTS"></span>**Ansprüchen**
</dt> <dd>

Eine Zeichenfolge, die die vom ACE kontrollierten [Zugriffsrechte](access-rights-and-access-masks.md) angibt. Diese Zeichenfolge kann eine hexadezimale Zeichen folgen Darstellung der Zugriffsrechte sein, z. b. "0x7800003F", oder es kann sich um eine Verkettung der folgenden Zeichen folgen handeln.



### <a name="generic-access-rights"></a>Generische Zugriffsrechte

| Zugriffsrechte Zeichenfolge | Konstante in SDDL. h | Zugriffsrechte Wert |
|----------------------|--------------------|--------------------|
| Gas                 | SDDL, \_ generisch \_ | generisch \_ alle       |
| G                 | allgemeiner SDDL- \_ \_ Lesevorgang | generischer \_ Lesevorgang     |
| GW                 | generischer SDDL- \_ \_ Schreibvorgang | generischer \_ Schreibvorgang |
| GX                 | Allgemeine SDDL- \_ \_ Ausführung | generisch \_ Ausführen |


### <a name="standard-access-rights"></a>Standard Zugriffsrechte

| Zugriffsrechte Zeichenfolge | Konstante in SDDL. h | Zugriffsrechte Wert |
|----------------------|--------------------|--------------------|
| RC                 | SDDL- \_ Lese \_ Steuerelement | Lese \_ Steuerelement      |
| Berichteten                 | SDDL- \_ Standard \_ Delete | Delete          |
| Zel                 | SDDL- \_ Schreib- \_ DAC | \_DAC schreiben            |
| WO                 | SDDL- \_ Schreib \_ Besitzer | \_Besitzer schreiben        |

### <a name="directory-service-object-access-rights"></a>Verzeichnisdienst-Objekt Zugriffsrechte

| Zugriffsrechte Zeichenfolge | Konstante in SDDL. h | Zugriffsrechte Wert |
|----------------------|--------------------|--------------------|
| Neutraler                 | SDDL- \_ Lese \_ Eigenschaft | ADS \_ right \_ DS \_ Read \_ Prop |
| UA                 | SDDL- \_ Schreib \_ Eigenschaft | ADS \_ right \_ DS \_ Schreib \_ Prop |
| 125                 | untergeordnetes SDDL-Element \_ Erstellen \_ | ADS \_ right \_ DS \_ Create \_ Child |
| DC                 | SDDL \_ Delete \_ Child | ADS \_ right \_ DS \_ Delete \_ Child |
| LTE                 | untergeordnete SDDL- \_ Listen \_ | Liste der AD \_ right \_ actrl \_ DS \_ |
| Erstellung                 | SDDL \_ selbst \_ schreiben    | ADS \_ right \_ DS \_ selbst |
| Siehe                  | SDDL- \_ Listen \_ Objekt | ADS \_ right \_ DS \_ List- \_ Objekt |
| DT                 | SDDL- \_ Lösch Struktur \_ | ADS \_ right \_ DS \_ Delete \_ Tree |
| Programmiert                  | SDDL- \_ Steuerungs \_ Zugriff | Anzeigen des Zugriffs auf die \_ \_ DS- \_ Steuerung \_ |

### <a name="file-access-rights"></a>Dateizugriffsrechte

| Zugriffsrechte Zeichenfolge | Konstante in SDDL. h | Zugriffsrechte Wert |
|----------------------|--------------------|--------------------|
| Übergangs                 | SDDL- \_ Datei \_ alle    | voll \_ Zugriff auf Datei \_   |
| Fr                 | SDDL- \_ Datei \_ Lesen   | \_generischer Datei \_ Lesevorgang |
| WL                 | SDDL- \_ Datei \_ Schreibvorgänge  | \_generischer Datei \_ Schreibvorgang |
| Designer                 | SDDL- \_ Datei \_ Ausführen | \_generische Datei \_ Ausführung |


### <a name="registry-key-access-rights"></a>Zugriffsrechte für den Registrierungsschlüssel

| Zugriffsrechte Zeichenfolge | Konstante in SDDL. h | Zugriffsrechte Wert |
|----------------------|--------------------|--------------------|
| At                 | Alle SDDL- \_ Schlüssel \_     | Schlüssel \_ \_ Zugriff   |
| Stechen                 | SDDL- \_ Schlüssel \_ Lesen    | Schlüssel \_ Lesevorgang          |
| 132                 | SDDL- \_ Schlüssel \_ Schreibvorgang   | Schlüssel \_ Schreibvorgang         |
| "Kx"                 | SDDL- \_ Schlüssel \_ Ausführung | Schlüssel \_ Ausführung       |

### <a name="mandatory-label-rights"></a>Obligatorische Bezeichnungs Rechte

| Zugriffsrechte Zeichenfolge | Konstante in SDDL. h | Zugriffsrechte Wert |
|----------------------|--------------------|--------------------|
| Nr.                 | SDDL wird \_ nicht \_ gelesen \_ | obligatorische Bezeichnung "System" wird \_ \_ \_ nicht \_ gelesen \_ |
| AUT                 | SDDL \_ nicht \_ schreiben \_ | erforderliche \_ System \_ Bezeichnung \_ kein \_ schreiben \_ |
| NX                 | SDDL wird \_ nicht \_ ausgeführt \_ | \_obligatorische System \_ Bezeichnung " \_ kein \_ Ausführen \_ " |
</dd> <dt>

<span id="object_guid"></span><span id="OBJECT_GUID"></span>**Objekt- \_ GUID**
</dt> <dd>

Eine Zeichen folgen Darstellung einer GUID, die den Wert des **ObjectType** -Members einer Objekt spezifischen ACE-Struktur angibt, z. b. [**Access \_ Allowed-Objekt- \_ \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace). Die GUID-Zeichenfolge verwendet das Format, das von der [**UUIDToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) -Funktion zurückgegeben wird.

In der folgenden Tabelle werden einige häufig verwendete Objekt-GUIDs aufgelistet.



| Rechte und GUID                         | Berechtigung      |
|-----------------------------------------|-----------------|
| CR; ab721a53-1e2f-11D0-9819-00aa0040529b | Kennwort ändern |
| CR; 00299570-246d-11D0-A768-00aa006e0529 | Kennwort zurücksetzen  |



 

</dd> <dt>

<span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**\_Objekt- \_ GUID erben**
</dt> <dd>

Eine Zeichen folgen Darstellung einer GUID, die den Wert des **erstellitedobjecttype** -Members einer Objekt spezifischen ACE-Struktur angibt. Die GUID-Zeichenfolge verwendet das [**UUIDToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) -Format.

</dd> <dt>

<span id="account_sid"></span><span id="ACCOUNT_SID"></span>**Konto- \_ sid**
</dt> <dd>

[Sid-Zeichenfolge](sid-strings.md) , die den Vertrauens [nehmer des ACE](trustees.md) identifiziert.

</dd> <dt>

<span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**Ressourcen \_ Attribut**
</dt> <dd>

\[Optional \] : das Ressourcen \_ Attribut gilt nur für Resource ACEs und ist optional. Eine Zeichenfolge, die den Datentyp angibt. Der ACE-Datentyp des Ressourcen Attributs kann einer der folgenden Datentypen sein, die in "SDDL. h" definiert sind.

Das \# Zeichen "" ist in Ressourcen Attributen mit "0" Synonym. Beispiel: d:Ai (XA; oici; FA;;; WD; (octetstringtype = = \# 1 \# 2 \# 3 \# \# )) entspricht und wird als d:Ai (XA; oici; FA;;;) interpretiert. WD; (octetstringtype = = \# 01020300)).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** Ressourcen Attribute sind nicht verfügbar.



| Ressourcen Attribut-ACE-Datentyp Zeichenfolge | Konstante in SDDL. h | Datentyp        |
|-----------------------------------------|--------------------|------------------|
| Kriegs                                    | SDDL \_ int          | Ganze Zahl mit Vorzeichen   |
| Di                                    | SDDL- \_ uint         | Ganze Zahl ohne Vorzeichen |
| TS                                    | SDDL \_ wstring      | Breite Zeichenfolge      |
| CT                                    | SDDL- \_ sid          | SID              |
| Llte                                    | SDDL- \_ BLOB         | Oktett-Zeichenfolge     |
| T                                    | SDDL- \_ boolescher Wert      | Boolean          |



 

</dd> </dl>

Das folgende Beispiel zeigt eine ACE-Zeichenfolge für einen Zugriffs zulässigen ACE. Es handelt sich nicht um einen Objekt spezifischen ACE, d. h., er enthält keine Informationen in den **Objekt- \_ GUID** und **erbt \_ Objekt- \_ GUID** -Felder. Das Feld **ACE \_ Flags** ist ebenfalls leer, was darauf hinweist, dass keines der ACE-Flags festgelegt ist.


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



Die oben gezeigte ACE-Zeichenfolge beschreibt die folgenden ACE-Informationen.


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



Im folgenden Beispiel wird eine Datei veranschaulicht, die mit Ressourcen Ansprüchen für Windows und Structured Query Language (SQL) klassifiziert ist, wobei das Geheimnis auf hohe geschäftliche Auswirkung festgelegt ist.


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



Die oben gezeigte ACE-Zeichenfolge beschreibt die folgenden ACE-Informationen.


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



Weitere Informationen finden Sie unter [Sicherheits Deskriptor-Zeichen folgen Format](security-descriptor-string-format.md) und [sid](sid-strings.md)-Zeichen folgen. Informationen zu bedingten ACEs finden Sie unter [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[\[MS-DYP \] : Beschreibung der Sicherheits Beschreibungssprache](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

