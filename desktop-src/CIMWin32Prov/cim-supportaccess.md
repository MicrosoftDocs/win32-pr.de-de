---
description: Die CIM \_ SupportAccess-Klasse definiert, wie Sie Unterstützung für ein Produkt erhalten.
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
ms.openlocfilehash: c53254b51b228efb2c1f14b7fb5f07475fb275d20c7df6444dc88e048bb1d30f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020908"
---
# <a name="cim_supportaccess-class"></a>CIM \_ SupportAccess-Klasse

Die **CIM \_ SupportAccess-Klasse** definiert, wie Sie Unterstützung für ein Produkt erhalten.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **CIM \_ SupportAccess-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SupportAccess-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CommunicationInfo**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 002.11", "MIF. DMTF \| FRU \| 002.12")
</dt> </dl>

Details zum Kommunikationsmodus. Wenn die **CommunicationMode-Eigenschaft** beispielsweise "Telefon" ist, gibt diese Eigenschaft die telefonnummer an, die sie anrufen soll.

</dd> <dt>

**CommunicationMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Unterstützung \| 001.5")
</dt> </dl>

Form der Kommunikation, die verwendet werden soll, um Support zu erhalten.

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

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Onlinedienst** (5)


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

E-Mail

</dd> </dl>

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Unterstützung \| 001.3")
</dt> </dl>

Textbeschreibung der Art der bereitgestellten Unterstützung.

</dd> <dt>

**Gebietsschema**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Unterstützung \| 001.2"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Geografische Region oder Sprachdialekt, auf die sich diese Unterstützungsressource bezieht.

</dd> <dt>

**SupportAccessId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Beliebige Freiformzeichenfolge, die vom Produkthersteller oder von der Organisation definiert wird, die das Produkt bereitgestellt. Diese Eigenschaft sollte im gesamten Unternehmen eindeutig sein, da es sich um einen Schlüssel handelt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

