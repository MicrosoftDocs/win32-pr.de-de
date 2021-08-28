---
description: Die Registrierung eines permanenten Ereignisverbraucher erfordert eine Instanz der \_ \_ EventFilter-Systemklasse.
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
ms.openlocfilehash: 2732366b75c383dc9ed86aa70ef5987fd5ac41beffb2b7e871a57ac6003cc72e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110626"
---
# <a name="__eventfilter-class"></a>\_\_EventFilter-Klasse

Die Registrierung eines permanenten Ereignisverbraucher erfordert eine Instanz der **\_ \_ EventFilter-Systemklasse.**

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ EventFilter-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ EventFilter-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Sicherheits-ID (SID), die den Benutzer, der diesen Filter erstellt, eindeutig identifiziert. Windows Die Verwaltungsinstrumentation (WMI) speichert je nach Betriebssystem die SID des Benutzers, der eine Instanz von **\_ \_ EventFilter** oder die Administrator-SID erstellt. Weitere Informationen finden Sie unter [Binden eines Ereignisfilters](binding-an-event-filter-with-a-logical-consumer.md) mit einem logischen Consumer und Überwachen und Reagieren auf [Ereignisse mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md)

</dd> <dt>

**EventAccess**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Sicherheitsdeskriptor (SD) in security descriptor Definition Language (SDDL), der den Zugriff auf Ereignisse steuert, die an den Filter übermittelt werden. Verwenden Sie diese Eigenschaft, um anzugeben, dass nur Ereignisse im Sicherheitskontext bestimmter Konten an diesen Filter übermittelt werden können. Beispielsweise kann ein permanenter Ereignisnutzer die Sicherheitsprotokolle nur löschen, wenn ein bestimmtes Ereignis von einem bestimmten Benutzer generiert wird. Um anzugeben, wer Ereignisse in diesem Filter veröffentlichen kann, verwenden Sie die **WBEM \_ RIGHT \_ PUBLISH-Maske** im Access Control Entry (ACE) für die [**SECURITY \_ DESCRIPTOR-Eigenschaft.**](--event.md) Weitere Informationen finden Sie unter [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language). Weitere Informationen zu Konstanten, die zum Festlegen dieses Sicherheitsdeskriptors verwendet werden, finden Sie unter [WMI-Sicherheitskonst constants](wmi-security-constants.md). Weitere Informationen und Beispiele finden Sie unter replace: Receiving Events Securely (Ersetzen:[Sicheres Empfangen von Ereignissen).](receiving-events-securely.md)

Sie können einen Ereigniszugriffssicherheitsdeskriptor so konfigurieren, dass ein Ereignis nur übermittelt werden kann, wenn das lokale Systemkonto das Ereignis generiert. Weitere Informationen zum Erstellen einer Sicherheitsbeschreibung und zum Autorisieren des Zugriffs finden Sie [unter Access Control](/windows/desktop/SecAuthZ/access-control).

Beispiel: Mit der folgenden SDDL-Zeichenfolge können nur Administratoren Ereignisse für den Filter bereitstellen. Das zum Bereitstellen von Ereignissen erforderliche Recht ist **WBEM \_ RIGHT \_ PUBLISH** (x80).


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

**EventNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Namespace der Ereignisinstanz, die für namespaceübergreifende Abonnements verwendet wird.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Eindeutiger Bezeichner eines Ereignisfilters. Da ein Ereignisfilter nur intern von WMI verwendet wird, wird empfohlen, diese Eigenschaft auf einen global eindeutigen Bezeichner **(GUID)** zu setzen, der in eine Zeichenfolge konvertiert wird. Benutzer können jedoch ein beliebiges privates Schema für einen Filternamen verwenden, solange kein Konflikt mit anderen Filtern besteht.

</dd> <dt>

**Abfrage**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Windows WQL-Ereignisabfrage (Management Instrumentation Query Language), die den Ereignissatz für die Consumerbenachrichtigung und die spezifischen Bedingungen für die Benachrichtigung angibt.

</dd> <dt>

**QueryLanguage**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Für die Abfrage verwendete Sprache. Da WMI derzeit nur WMI Query Language (WQL) als Abfragesprache unterstützt, muss diese Eigenschaft auf "WQL" festgelegt werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ EventFilter-Klasse** wird von [**\_ \_ IndicationRelated abgeleitet.**](--indicationrelated.md)

## <a name="examples"></a>Beispiele

Im [PowerShell-Beispiel](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) Create Permanent WMI Event registration to monitor files (Erstellen einer permanenten WMI-Ereignisregistrierung zum Überwachen von Dateien) im TechNet-Katalog wird **\_ \_ EventFilter** als Teil eines komplexen Skripts verwendet, um eine permanente WMI-Ereignisregistrierung zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[Erstellen eines Ereignisfilters](creating-an-event-filter.md)
</dt> <dt>

[Jederzeites Empfangen von Ereignissen](receiving-events-at-all-times.md)
</dt> <dt>

[Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Überwachen von Ereignissen](monitoring-events.md)
</dt> <dt>

[Standard-Consumerklassen](standard-consumer-classes.md)
</dt> <dt>

[Sichern von WMI-Ereignissen](securing-wmi-events.md)
</dt> </dl>

 

