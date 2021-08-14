---
description: Erläutert die Zeichenfolgen, die in einem Zugriffssteuerungseintrag verwendet werden.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: ACE-Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60e8f4f5d3cd94f6e871b3b4962d2d548afa003c3bd4aa37a1ae8f008ce1a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785401"
---
# <a name="ace-strings"></a>ACE-Zeichenfolgen

Die [Sicherheitsdeskriptordefinitionssprache (Security Descriptor Definition Language,](security-descriptor-definition-language.md) SDDL) verwendet ACE-Zeichenfolgen in den DACL- und SACL-Komponenten einer [*Sicherheitsbeschreibungszeichenfolge.*](/windows/desktop/SecGloss/s-gly)

Wie in den Beispielen zum [Sicherheitsdeskriptorzeichenfolgenformat](security-descriptor-string-format.md) gezeigt, wird jeder ACE in einer Sicherheitsdeskriptorzeichenfolge in Klammern eingeschlossen. Die Felder des ACE befinden sich in der folgenden Reihenfolge und werden durch Semikolons (;).

> [!Note]  
> Es gibt ein anderes Format für [*bedingte Zugriffssteuerungseinträge*](/windows/desktop/SecGloss/a-gly) (Conditional Access Control Entries, ACEs) als für andere ACE-Typen. Informationen zu bedingten ACEs finden Sie unter [Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs.](security-descriptor-definition-language-for-conditional-aces-.md)

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a>Felder

<dl> <dt>

<span id="ace_type"></span><span id="ACE_TYPE"></span>**\_ace-Typ**
</dt> <dd>

Eine Zeichenfolge, die den Wert des **AceType-Elements** der [**ACE \_ HEADER-Struktur**](/windows/desktop/api/Winnt/ns-winnt-ace_header) angibt. Die ACE-Typzeichenfolge kann eine der folgenden Zeichenfolgen sein, die in Sddl.h definiert sind.



| ACE-Typzeichenfolge | Konstante in "Sddl.h"                      | AceType-Wert                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| „A“             | \_SDDL-ZUGRIFF \_ ZULÄSSIG                   | \_ZUGRIFF \_ ZULÄSSIGER \_ ACE-TYP                                                                                                                                         |
| "D"             | SDDL \_ ACCESS \_ DENIED                    | ACE-TYP "ZUGRIFF \_ \_ \_ VERWEIGERT"                                                                                                                                          |
| "OA"            | \_SDDL-OBJEKTZUGRIFF \_ \_ ZULÄSSIG           | \_ \_ ZUGRIFFSBERECHTIGUNGSTYP FÜR \_ \_ OBJEKTASSET                                                                                                                                 |
| "OD"            | ZUGRIFF \_ AUF SDDL-OBJEKT \_ \_ VERWEIGERT            | ACCESS \_ DENIED \_ OBJECT \_ ACE \_ TYPE                                                                                                                                  |
| "AU"            | SDDL \_ AUDIT                             | ACE-TYP DER \_ SYSTEMÜBERWACHUNG \_ \_                                                                                                                                           |
| "AL"            | SDDL \_ ALARM                             | ACE-TYP DES \_ SYSTEMALARMS \_ \_                                                                                                                                           |
| "OU"            | \_SDDL-OBJEKTÜBERWACHUNG \_                     | \_ \_ ACE-TYP DES SYSTEMÜBERWACHUNGSOBJEKTS \_ \_                                                                                                                                   |
| "OL"            | \_ \_ SDDL-OBJEKTALARM                     | ACE-TYP DES \_ SYSTEMALARMOBJEKTS \_ \_ \_                                                                                                                                   |
| "ML"            | OBLIGATORISCHE \_ \_ SDDL-BEZEICHNUNG                  | \_SYSTEM MANDATORY LABEL ACE TYPE Windows Server \_ \_ \_ **2003:** Nicht verfügbar.                                                                                        |
| "XA"            | SDDL \_ CALLBACK \_ ACCESS \_ ALLOWED         | ZUGRIFF \_ ZULÄSSIGER \_ RÜCKRUF \_ \_ ACE-TYP **Windows Server 2008, Windows Vista und Windows Server 2003:** Nicht verfügbar.                                                |
| "XD"            | ZUGRIFF DES \_ SDDL-RÜCKRUFS \_ \_ VERWEIGERT          | ZUGRIFF \_ VERWEIGERT RÜCKRUF ACE TYPE Windows Server \_ \_ \_ **2008, Windows Vista und Windows Server 2003:** Nicht verfügbar.                                                 |
| "RA"            | \_ \_ SDDL-RESSOURCENATTRIBUT               | ACE-TYP DES \_ \_ \_ \_ SYSTEMRESSOURCENATTRIBUTS **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** Nicht verfügbar.<br/> |
| "SP"            | SDDL \_ SCOPED \_ POLICY \_ ID                | ACE-TYP DER \_ SYSTEMWEITEN \_ \_ RICHTLINIEN-ID \_ Windows Server \_ **2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** Nicht verfügbar.<br/>  |
| "XU"            | SDDL \_ CALLBACK \_ AUDIT                   | SYSTEM \_ AUDIT \_ CALLBACK ACE TYPE Windows Server \_ \_ **2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** Nicht verfügbar.<br/>     |
| "ZA"            | ZUGRIFF \_ AUF SDDL-RÜCKRUFOBJEKTE \_ \_ \_ ZULÄSSIG | ZUGRIFF \_ ZULÄSSIGER \_ RÜCKRUF \_ \_ ACE-TYP **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** Nicht verfügbar.<br/>   |
| "TL"            | \_ \_ SDDL-PROZESSVERTRAUENSBEZEICHNUNG \_             | SYSTEM \_ PROCESS TRUST LABEL ACE TYPE \_ \_ \_ \_ **Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** Nicht verfügbar. |
| "FL"            | \_SDDL-ZUGRIFFSFILTER \_                    | ACE-TYP DES \_ SYSTEMZUGRIFFSFILTERS \_ \_ \_ **Windows Server 2016, Windows 10 Version 1607, Windows 10 Version 1511, Windows 10 Version 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** Nicht verfügbar. |
 

> [!Note]  
> Wenn **der \_ ace-Typ** ACCESS ALLOWED OBJECT ACE TYPE ist \_ und weder \_ \_ \_ **\_ objekt-GUID** noch **\_ \_ objekt-GUID erben** eine [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) angegeben hat, konvertiert [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) **den \_ Ace-Typ** in ACCESS \_ ALLOWED ACE \_ \_ TYPE.

 

</dd> <dt>

<span id="ace_flags"></span><span id="ACE_FLAGS"></span>**\_Ace-Flags**
</dt> <dd>

Eine Zeichenfolge, die den Wert des **AceFlags-Members** der [**ACE \_ HEADER-Struktur**](/windows/desktop/api/Winnt/ns-winnt-ace_header) angibt. Die ACE-Flagzeichenfolge kann eine Verkettung der folgenden Zeichenfolgen sein, die in Sddl.h definiert sind.



| ACE-Flagzeichenfolge | Konstante in "Sddl.h"       | AceFlag-Wert                 |
|------------------|--------------------------|-------------------------------|
| "CI"             | \_SDDL-CONTAINER \_ ERBEN | CONTAINER \_ INHERIT \_ ACE       |
| "OI"             | \_SDDL-OBJEKT \_ ERBEN    | \_OBJEKTVERERBUNGS-ACE \_          |
| "NP"             | SDDL \_ NO \_ PROPAGATE      | NO \_ PROPAGATE \_ INHERIT \_ ACE   |
| "E/A"             | NUR SDDL \_ \_ ERBEN      | \_NUR ACE ERBEN \_            |
| „ID“             | SDDL \_ GEERBT          | GEERBTER \_ ACE                |
| "SA"             | SDDL \_ AUDIT \_ SUCCESS     | ACE-FLAG FÜR \_ ERFOLGREICHEN ZUGRIFF \_ \_ |
| "FA"             | FEHLER BEI DER \_ SDDL-ÜBERWACHUNG \_     | ACE-FLAG FÜR \_ FEHLGESCHLAGENEN ZUGRIFF \_ \_     |
| "TP"             | SDDL \_ TRUST \_ PROTECTED \_ FILTER | WINDOWS SERVER 2016 \_ DES ACE-FLAGS FÜR GESCHÜTZTE \_ FILTER \_ \_ **VERTRAUEN, Windows 10 Version 1607, Windows 10 Version 1511, Windows 10 Version 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** Nicht verfügbar. |
| "CR"             | SDDL \_ CRITICAL           | CRITICAL \_ ACE FLAG Windows Server Version \_ **1803, Windows 10 Version 1803, Windows Server Version 1709, Windows 10 Version 1709, Windows 10 Version 1703, Windows Server 2016, Windows 10 Version 1607, Windows 10 Version 1511, Windows 10 Version 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** Nicht verfügbar. |
 

</dd> <dt>

<span id="rights"></span><span id="RIGHTS"></span>**Rechte**
</dt> <dd>

Eine Zeichenfolge, die die vom ACE gesteuerten [Zugriffsrechte](access-rights-and-access-masks.md) angibt. Diese Zeichenfolge kann eine hexadezimale Zeichenfolgendarstellung der Zugriffsrechte sein, z. B. "0x7800003F", oder sie kann eine Verkettung der folgenden Zeichenfolgen sein.



### <a name="generic-access-rights"></a>Allgemeine Zugriffsrechte

| Zugriffsberechtigungszeichenfolge | Konstante in "Sddl.h" | Zugriffsrechtwert |
|----------------------|--------------------|--------------------|
| "GA"                 | SDDL \_ GENERIC \_ ALL | GENERIC \_ ALL       |
| "GR"                 | SDDL \_ GENERIC \_ READ | GENERISCHER \_ LESE-     |
| "GW"                 | SDDL \_ GENERIC \_ WRITE | GENERISCHER \_ SCHREIBVORGANG |
| "GX"                 | SDDL \_ GENERIC \_ EXECUTE | GENERIC \_ EXECUTE |


### <a name="standard-access-rights"></a>Standardzugriffsrechte

| Zugriffsberechtigungszeichenfolge | Konstante in "Sddl.h" | Zugriffsrechtwert |
|----------------------|--------------------|--------------------|
| "RC"                 | \_ \_ SDDL-LESESTEUERELEMENT | \_READ-STEUERELEMENT      |
| "SD"                 | SDDL \_ STANDARD \_ DELETE | Delete          |
| "WD"                 | SDDL \_ WRITE \_ DAC | \_SCHREIB-DAC            |
| "WO"                 | SDDL \_ WRITE \_ OWNER | WRITE \_ OWNER        |

### <a name="directory-service-object-access-rights"></a>Zugriffsrechte für Verzeichnisdienstobjekte

| Zugriffsberechtigungszeichenfolge | Konstante in "Sddl.h" | Zugriffsrechtwert |
|----------------------|--------------------|--------------------|
| "RP"                 | \_SDDL-LESEEIGENSCHAFT \_ | ADS \_ RIGHT \_ DS \_ READ \_ PROP |
| "WP"                 | SDDL \_ \_ WRITE-EIGENSCHAFT | ADS \_ RIGHT \_ DS \_ WRITE \_ PROP |
| "CC"                 | SDDL \_ CREATE \_ CHILD | ADS \_ RIGHT \_ DS \_ CREATE \_ CHILD |
| "DC"                 | UNTERGEORDNETES \_ SDDL-LÖSCHEN \_ | ADS \_ RIGHT \_ DS \_ DELETE \_ CHILD |
| "LC"                 | UNTERGEORDNETE \_ SDDL-LISTEN \_ | ADS \_ RIGHT \_ ACTRL \_ DS \_ LIST |
| "SW"                 | SDDL \_ SELF \_ WRITE    | ADS \_ RIGHT \_ DS \_ SELF |
| "LO"                  | SDDL \_ \_ LIST-OBJEKT | ADS \_ RIGHT \_ DS \_ LIST \_ OBJECT |
| "DT"                 | SDDL \_ DELETE \_ TREE | ADS \_ RIGHT \_ DS \_ DELETE \_ TREE |
| "CR"                  | SDDL \_ CONTROL \_ ACCESS | ADS \_ RIGHT \_ DS \_ CONTROL \_ ACCESS |

### <a name="file-access-rights"></a>Dateizugriffsrechte

| Zugriffsberechtigungszeichenfolge | Konstante in "Sddl.h" | Zugriffsrechtwert |
|----------------------|--------------------|--------------------|
| "FA"                 | SDDL \_ FILE \_ ALL    | FILE \_ ALL \_ ACCESS   |
| "FR"                 | LESEN VON \_ SDDL-DATEIEN \_   | \_GENERISCHER \_ DATEILESEDATENLESE-ARTIKEL |
| "FW"                 | \_ \_ SDDL-DATEISCHREIBVORGANG  | \_GENERISCHER \_ DATEISCHREIBVORGANG |
| "FX"                 | SDDL \_ FILE \_ EXECUTE | GENERISCHE \_ \_ DATEIAUSFÜHRUNG |


### <a name="registry-key-access-rights"></a>Zugriffsrechte für Registrierungsschlüssel

| Zugriffsberechtigungszeichenfolge | Konstante in "Sddl.h" | Zugriffsrechtwert |
|----------------------|--------------------|--------------------|
| "KA"                 | SDDL \_ KEY \_ ALL     | KEY \_ ALL \_ ACCESS   |
| "KR"                 | LESEN DES \_ SDDL-SCHLÜSSELS \_    | KEY \_ READ          |
| "KW"                 | SCHREIBEN VON \_ SDDL-SCHLÜSSELN \_   | KEY \_ WRITE         |
| "KX"                 | SDDL \_ KEY \_ EXECUTE | KEY \_ EXECUTE       |

### <a name="mandatory-label-rights"></a>Obligatorische Bezeichnungsrechte

| Zugriffsberechtigungszeichenfolge | Konstante in "Sddl.h" | Zugriffsrechtwert |
|----------------------|--------------------|--------------------|
| "NR"                 | SDDL \_ NO \_ READ \_ UP | \_SYSTEM MANDATORY LABEL NO READ UP Windows Server \_ \_ \_ \_ **2008, Windows Vista and Windows Server 2003:** Not available. |
| "NW"                 | SDDL \_ OHNE \_ \_ SCHREIBZUGRIFF | \_SYSTEM MANDATORY LABEL NO WRITE UP Windows Server \_ \_ \_ \_ **2008, Windows Vista and Windows Server 2003:** Not available. |
| "NX"                 | SDDL \_ NO \_ EXECUTE \_ UP | \_SYSTEM MANDATORY LABEL NO EXECUTE UP Windows Server \_ \_ \_ \_ **2008, Windows Vista and Windows Server 2003:** Not available. |
</dd> <dt>

<span id="object_guid"></span><span id="OBJECT_GUID"></span>**\_Objekt-GUID**
</dt> <dd>

Eine Zeichenfolgendarstellung einer GUID, die den Wert des **ObjectType-Members** einer objektspezifischen ACE-Struktur angibt, z. B. [**ACCESS ALLOWED OBJECT \_ \_ \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace). Die GUID-Zeichenfolge verwendet das format, das von der [**UuidToString-Funktion**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) zurückgegeben wird.

In der folgenden Tabelle sind einige häufig verwendete Objekt-GUIDs aufgeführt.



| Rechte und GUID                         | Berechtigung      |
|-----------------------------------------|-----------------|
| CR;ab721a53-1e2f-11d0-9819-00aa0040529b | Kennwort ändern |
| CR;00299570-246d-11d0-a768-00aa006e0529 | Kennwort zurücksetzen  |



 

</dd> <dt>

<span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**\_Erben der \_ Objekt-GUID**
</dt> <dd>

Eine Zeichenfolgendarstellung einer GUID, die den Wert des **InheritedObjectType-Elements** einer objektspezifischen ACE-Struktur angibt. Die GUID-Zeichenfolge verwendet das [**UuidToString-Format.**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring)

</dd> <dt>

<span id="account_sid"></span><span id="ACCOUNT_SID"></span>**account \_ sid**
</dt> <dd>

[SID-Zeichenfolge,](sid-strings.md) die den [Vertrauensnehmer](trustees.md) des ACE identifiziert.

</dd> <dt>

<span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**\_Ressourcenattribut**
</dt> <dd>

\[OPTIONAL \] Das \_ Ressourcenattribut ist nur für Ressourcen-ACEs und optional. Eine Zeichenfolge, die den Datentyp angibt. Der Ace-Datentyp des Ressourcenattributs kann einer der folgenden Datentypen sein, die in Sddl.h definiert sind.

Das \# Zeichen "" ist synonym mit "0" in Ressourcenattributen. Beispiel: D:AI(XA;OICI;FA;;; WD;(OctetStringType== \# 1 \# 2 \# 3 \# \# )) entspricht und wird als D:AI(XA;OICI;FA;;; interpretiert. WD;(OctetStringType== \# 01020300)).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista und Windows Server 2003:** Ressourcenattribute sind nicht verfügbar.



| Ace-Datentypzeichenfolge für Ressourcenattribut | Konstante in "Sddl.h" | Datentyp        |
|-----------------------------------------|--------------------|------------------|
| "TI"                                    | SDDL \_ INT          | Ganze Zahl mit Vorzeichen   |
| "TU"                                    | SDDL \_ UINT         | Ganze Zahl ohne Vorzeichen |
| "TS"                                    | SDDL \_ WSTRING      | Breite Zeichenfolge      |
| "TD"                                    | \_SDDL-SID          | SID              |
| "TX"                                    | \_SDDL-BLOB         | Oktettzeichenfolge     |
| "TB"                                    | SDDL \_ BOOLEAN      | Boolean          |



 

</dd> </dl>

Das folgende Beispiel zeigt eine ACE-Zeichenfolge für einen zugriffsberechtigten ACE. Da es sich nicht um einen objektspezifischen ACE handelt, enthält er keine Informationen in der **\_ Objekt-GUID** und **erbt \_ \_ Objekt-GUID-Felder.** Das Feld **ace \_ flags** ist ebenfalls leer, was angibt, dass keines der ACE-Flags festgelegt ist.


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



Das folgende Beispiel zeigt eine Datei, die mit Ressourcenansprüchen für Windows und strukturierte Abfragesprache (SQL) klassifiziert ist, wobei Secrecy auf High Business Impact festgelegt ist.


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



Weitere Informationen finden Sie unter [Security Descriptor String Format (Format der Sicherheitsbeschreibungszeichenfolge)](security-descriptor-string-format.md) und [SID Strings (SID-Zeichenfolgen).](sid-strings.md) Informationen zu bedingten ACEs finden Sie unter [Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs.](security-descriptor-definition-language-for-conditional-aces-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[\[MS-DTYP: \] Beschreibungssprache des Sicherheitsdeskriptors](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

