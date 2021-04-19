---
description: Die Registrierung eines permanenten Ereignisconsumers erfordert eine Instanz der \_ \_ EventFilter-System Klasse.
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: __EventFilter-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349520"
---
# <a name="__eventfilter-class"></a>\_\_EventFilter-Klasse

Die Registrierung eines permanenten **\_ \_ Ereignisconsumers** erfordert eine Instanz der EventFilter-System Klasse.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a>Member

Die **\_ \_ EventFilter** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ EventFilter** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**"Kreatorsid"**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Sicherheits-ID (SID), die den Benutzer, der diesen Filter erstellt, eindeutig identifiziert. Windows-Verwaltungsinstrumentation (WMI) speichert die SID des Benutzers, der eine Instanz von **\_ \_ EventFilter** oder die Administrator-SID erstellt, je nach Betriebssystem. Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

</dd> <dt>

**Eventaccess**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Sicherheits Beschreibung (SD) in Security Deskriptor Definition Language (SDDL), die den Zugriff auf Ereignisse steuert, die an den Filter übermittelt werden. Verwenden Sie diese Eigenschaft, um anzugeben, dass nur Ereignisse im Sicherheitskontext bestimmter Konten an diesen Filter übermittelt werden können. Beispielsweise kann ein dauerhafter Ereignisconsumer die Sicherheitsprotokolle nur dann löschen, wenn ein bestimmtes Ereignis von einem bestimmten Benutzer generiert wird. Um anzugeben, wer Ereignisse in diesem Filter veröffentlichen kann, verwenden Sie die **WBEM \_ right- \_ Veröffentlichungs** Maske im Access Control Entry (ACE) für die [**\_ sicherheitsbeschreibungenschaft**](--event.md) . Weitere Informationen finden Sie unter [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language). Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](wmi-security-constants.md). Weitere Informationen und Beispiele finden Sie unter ersetzen:[sicheres empfangen von Ereignissen](receiving-events-securely.md).

Sie können einen Sicherheits Deskriptor für den Ereignis Zugriff konfigurieren, um zuzulassen, dass ein Ereignis nur dann übermittelt wird, wenn das lokale Systemkonto das Ereignis generiert. Weitere Informationen zum Erstellen einer Sicherheits Beschreibung und zum Autorisierungs Zugriff finden Sie unter [Access Control](/windows/desktop/SecAuthZ/access-control).

Beispiel: mit der folgenden SDDL-Zeichenfolge können nur Administratoren Ereignisse für den Filter bereitstellen. Die zum Bereitstellen von Ereignissen erforderliche Berechtigung ist **WBEM \_ right \_ Publish** (x80).


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

**Eventnamespace**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Namespace der Ereignis Instanz, die für Namespace übergreifende Abonnements verwendet wird.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Eindeutiger Bezeichner eines Ereignis Filters. Da ein Ereignis Filter nur intern von WMI verwendet wird, empfiehlt es sich, diese Eigenschaft auf eine in eine Zeichenfolge konvertierte Globally Unique Identifier (**GUID**) festzulegen. Consumer können jedoch ein beliebiges privates Schema für einen Filternamen verwenden, solange kein Konflikt mit anderen Filtern vorliegt.

</dd> <dt>

**Abfrage**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die WQL-Ereignis Abfrage (Windows-Verwaltungsinstrumentation Query Language), die den Satz von Ereignissen für die Consumer-Benachrichtigung angibt, sowie die spezifischen Benachrichtigungs Bedingungen.

</dd> <dt>

**QueryLanguage**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Sprache, die für die Abfrage verwendet wird. Da WMI derzeit nur WMI Query Language (WQL) als Abfragesprache unterstützt, muss diese Eigenschaft auf "WQL" festgelegt werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ EventFilter** -Klasse wird von " [**\_ \_ bezeichationrelated**](--indicationrelated.md)" abgeleitet.

## <a name="examples"></a>Beispiele

Das PowerShell-Beispiel zum [Erstellen einer permanenten WMI-Ereignis Registrierung zum Überwachen von Dateien](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) in der TechNet Gallery verwendet **\_ \_ EventFilter** als Teil eines komplexen Skripts, um eine permanente WMI-Ereignis Registrierung einzurichten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Indicationrelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Erstellen eines Ereignis Filters](creating-an-event-filter.md)
</dt> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> <dt>

[Überwachen von und reagieren auf Ereignisse mit Standard Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Überwachen von Ereignissen](monitoring-events.md)
</dt> <dt>

[Standard Consumer-Klassen](standard-consumer-classes.md)
</dt> <dt>

[Sichern von WMI-Ereignissen](securing-wmi-events.md)
</dt> </dl>

 

