---
description: Optionale Qualifizierer behandeln wiederkehrende Situationen, die nicht für alle CIM-kompatiblen Implementierungen gelten, die für die Interpretation dieser Qualifizierer nicht erforderlich sind.
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: Optionale Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351081"
---
# <a name="optional-qualifiers"></a>Optionale Qualifizierer

Optionale Qualifizierer behandeln wiederkehrende Situationen, die nicht für alle CIM-kompatiblen Implementierungen gelten, die für die Interpretation dieser Qualifizierer nicht erforderlich sind. Optionale Qualifizierer werden in der Spezifikation bereitgestellt, um zufällige benutzerdefinierte Qualifizierer zu vermeiden, die in diesen wiederkehrenden Situationen auftreten können.

<dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Lösch**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Zuordnungen, Verweise

Gibt für Zuordnungen an, ob die qualifizierte Zuordnung gelöscht werden muss, wenn eines der Objekte, auf die in der Zuordnung verwiesen wird, gelöscht wird und das entsprechende Objekt, auf das in der Zuordnung verwiesen wird, mit **ifdeleted** qualifiziert ist. Der Standardwert ist **false**.

Bei verweisen gibt dieser Qualifizierer an, ob das Objekt, auf das verwiesen wird, gelöscht werden muss, wenn die Zuordnung, die den Verweis enthält, gelöscht **und mit** **ifdeleted** qualifiziert wird, oder wenn eines der Objekte, auf die in der Zuordnung verwiesen wird, gelöscht wird und das entsprechende Objekt, auf das in der Zuordnung verwiesen wird

Verwendung: Anwendungen müssen mit dem **Delete** -Qualifizierer markierte Zuordnungen und Verweise nachverfolgen und die Zuordnung oder den Verweis entsprechend löschen. Wenn ein Objekt in der Zuordnung gelöscht, aber nicht mit **ifdeleted** gekennzeichnet wurde, sollte die Zuordnung nicht gelöscht werden.

Diese Verwendungs Regel muss überprüft werden, wenn das CIM-Sicherheitsmodell definiert ist.

</dd> <dt>

<span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Eres**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Eigenschaften, Verweise, Klassen, Zuordnungen, Methoden

Gibt an, ob die implizite Aktion eine umfangreiche Berechnung erfordert. Der Standardwert ist **false**.

</dd> <dt>

<span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**Ifdeleted**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Zuordnungen und Verweise

Gibt an, ob alle Objekte innerhalb einer durch **Delete** gekennzeichneten Zuordnung gelöscht werden müssen, wenn das Objekt, auf das verwiesen wird, oder die Zuordnung gelöscht wird. Der Standardwert ist **false**.

</dd> <dt>

<span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Zierenden**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Eigenschaften, Methoden

Gibt an, ob eine Klassen Eigenschaft indiziert werden soll. Dies hat bei der Anwendung auf Eigenschaften in Klassen, die vom Repository gehostet werden, nur die Bedeutung, dass (zum Zeitpunkt der Klassen Erstellung) eine schnelle sekundäre Abfrage Suche für diese Eigenschaft erstellt wird.

Nur der Wert **true** (Standard) ist zulässig.

</dd> <dt>

<span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Unsichtbar**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Zuordnungen, Eigenschaften, Methoden, Verweise, Klassen

Gibt an, ob die Zuordnung nur für interne Zwecke definiert ist (z. b. für die Definition der Abhängigkeits Semantik) und nicht angezeigt werden soll (z. b. in Maps). Der Standardwert ist **false**.

</dd> <dt>

<span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Viele**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Eigenschaften, Klassen

Gibt an, ob für die Eigenschaft oder Klasse eine große Menge an Speicherplatz erforderlich ist. Der Standardwert ist **false**.

</dd> <dt>

<span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Nicht \_ null**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: Eigenschaften

Gibt an, ob eine Klassen Eigenschaft einen **null** -Wert (**VT \_ null**) nicht annehmen kann. Nur der Wert **true** (Standard) ist zulässig.

Wenn dieser Qualifizierer angegeben wird, lässt WMI keine Erstellung von-Instanzen zu, deren-Eigenschaft auf **null** festgelegt ist, und **null** -Eigenschaften geben den Fehlercode " **WBEM \_ E unzulässig \_ \_ null** " zurück.

Beachten Sie, dass der [**Schlüssel**](standard-qualifiers.md) und die **indizierten** Qualifizierer dieses Verhalten bereits implizieren.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Ab**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: beliebig

Gibt an, dass das Schema Element dynamisch ist und daher von einem Anbieter aufgefüllt wird. Der Standardwert ist **null**. Dieser Qualifizierer ist ein Implementierungs spezifisches Handle der Instrumentierung.

</dd> <dt>

<span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Eller**
</dt> <dd>

Datentyp: **boolescher** Wert

Gilt für: beliebig

Gibt an, dass das angegebene Element als Teil einer zukünftigen Freigabe der CIM-Schemas vorgeschlagen wurde, aber noch nicht Teil des Standard Schemas ist. Stattdessen ist das-Element zum Experimentieren, implementieren und Bereitstellen von Feedback für Benutzer verfügbar. Basierend auf dem Feedback kann das Element dem Standard hinzugefügt werden, wie er dargestellt, geändert oder entfernt wird. Der Standardwert ist **false**. Eine-Implementierung muss kein Element mit diesem Qualifizierer unterstützen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften, Verweise, Methoden, Parameter

Ein bestimmter Typ, der einem Datenelement zugewiesen ist. Der Standardwert ist **null**.

Verwendung: der **syntaxtype** -Qualifizierer muss mit diesem Qualifizierer verwendet werden.

</dd> <dt>

<span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**Syntaxtype**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Eigenschaften, Verweise, Methoden, Parameter

Das Format des **Syntax** Qualifizierers. Der Standardwert ist **null**.

Verwendung: Sie müssen den **Syntax** Qualifizierer mit diesem Qualifizierer verwenden.

</dd> <dt>

<span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**
</dt> <dd>

Datentyp: **Zeichenfolge**

Gilt für: Klassen, Eigenschaften, Methoden, Zuordnungen, Hinweise, Verweise

Umstände, unter denen ein-Fehler ausgelöst wird. Der Standardwert ist **null**. Die Auslösertypen variieren je nach metamodellkonstrukt.

Für Klassen und Zuordnungen lauten die folgenden zulässigen Werte:

Erstellen

Löschen

Aktualisieren

Access

Für Eigenschaften und Verweise lauten die zulässigen Werte: Update und Access.

Bei-Methoden sind die zulässigen Werte vor und nach.

Für Hinweise wird der zulässige Wert ausgelöst.

</dd> <dt>

<span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**Unknownvalues**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Gilt für: Eigenschaften

Ein Satz von Werten, der angibt, dass der Wert der zugeordneten Eigenschaft unbekannt ist (die Eigenschaft kann nicht als gültiger oder sinnvoller Wert angesehen werden). Der Standardwert ist **null**.

Die Konventionen und Einschränkungen, die zum Definieren unbekannter Werte verwendet werden, entsprechen den Konventionen für den [**ValueMap**](standard-qualifiers.md) -Qualifizierer.

Beachten Sie, dass dieser Qualifizierer nicht überschrieben werden kann. Es ist nicht sinnvoll, einer Unterklasse das Behandeln eines Werts als bekannten Wert zu gestatten, wenn er von einer übergeordneten Klasse als unbekannt behandelt wird.

</dd> <dt>

<span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**Unsupportedvalues**
</dt> <dd>

Datentyp: **Zeichen folgen Array**

Gilt für: Eigenschaften

Ein Satz von Werten, der angibt, dass der Wert der zugeordneten Eigenschaft nicht unterstützt wird (die Eigenschaft kann nicht als gültiger oder sinnvoller Wert angesehen werden). Der Standardwert ist **null**.

Die Konventionen und Einschränkungen, die für die Definition nicht unterstützter Werte verwendet werden, entsprechen den Konventionen für den [**ValueMap**](standard-qualifiers.md) -Qualifizierer.

Hinweis Dieser Qualifizierer kann nicht überschrieben werden. Es ist nicht sinnvoll, einer Unterklasse das Behandeln eines Werts als unterstützten Wert zu gestatten, der von einer übergeordneten Klasse als unbekannt behandelt wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI Qualifizierer](wmi-qualifiers.md)
</dt> <dt>

[Fügen eines Qualifizierers](adding-a-qualifier.md)
</dt> </dl>

 

 




