---
description: Die CIM \_ supportaccess-Klasse definiert, wie Sie Unterstützung für ein Produkt erhalten.
ms.assetid: f42a793f-d71e-498e-9c6b-581aa029a0dd
ms.tgt_platform: multiple
title: CIM_SupportAccess-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SupportAccess
- CIM_SupportAccess.CommunicationInfo
- CIM_SupportAccess.CommunicationMode
- CIM_SupportAccess.Description
- CIM_SupportAccess.Locale
- CIM_SupportAccess.SupportAccessId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db5f1dc4331bd50e2fc61899f9d45fe2cdb0eca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126872"
---
# <a name="cim_supportaccess-class"></a>CIM- \_ supportaccess-Klasse

Die **CIM \_ supportaccess** -Klasse definiert, wie Sie Unterstützung für ein Produkt erhalten.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{80321714-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_SupportAccess
{
  string CommunicationInfo;
  uint16 CommunicationMode;
  string Description;
  string Locale;
  string SupportAccessId;
};
```

## <a name="members"></a>Member

Die **CIM- \_ supportaccess** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ supportaccess** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Communicationinfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| FRU \| 002,11 "," MIF. DMTF \| FRU \| 002,12 ")
</dt> </dl>

Details zum Kommunikationsmodus. Wenn die **communicationmode** -Eigenschaft z. b. "Phone" ist, gibt diese Eigenschaft die Telefonnummer an, die aufgerufen werden soll.

</dd> <dt>

**Communicationmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Unterstützung \| 001,5 ")
</dt> </dl>

Form der Kommunikation, die zum Abrufen von Support verwendet werden soll.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Telefon** (2)


</dt> <dd></dd> <dt>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)


</dt> <dd></dd> <dt>

<span id="BBS"></span><span id="bbs"></span>

<span id="BBS"></span><span id="bbs"></span>**BBS** (4)


</dt> <dd></dd> <dt>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Online Dienst** (5)


</dt> <dd></dd> <dt>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Webseite** (6)


</dt> <dd>

Webseite

</dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span id="FTP"></span><span id="ftp"></span>**FTP** (7)


</dt> <dd></dd> <dt>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**E-Mail** (8)


</dt> <dd>

Email

</dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Unterstützung \| 001,3 ")
</dt> </dl>

Textbeschreibung des angegebenen Unterstützungs Typs.

</dd> <dt>

**Gebietsschema**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Unterstützung \| 001,2 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Geografische Region oder sprach Dialekt, auf den sich diese Ressource bezieht.

</dd> <dt>

**SupportAccessID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Eine beliebige frei Form Zeichenfolge, die vom Produkthersteller oder von der Organisation definiert wird, die das Produkt bereitstellt. Diese Eigenschaft, da es sich um einen Schlüssel handelt, sollte im gesamten Unternehmen eindeutig sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

