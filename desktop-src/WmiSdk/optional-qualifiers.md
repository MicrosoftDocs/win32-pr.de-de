---
description: Optionale Qualifizierer beheben wiederkehrende Situationen, die nicht für alle CIM-konformen Implementierungen gelten, die nicht zum Interpretieren dieser Qualifizierer erforderlich sind.
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
ms.openlocfilehash: 05cd80cbccf2c67baaeac2982c896a0c74ead227619bfb17517a039fadf24a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050538"
---
# <a name="optional-qualifiers"></a>Optionale Qualifizierer

Optionale Qualifizierer beheben wiederkehrende Situationen, die nicht für alle CIM-konformen Implementierungen gelten, die nicht zum Interpretieren dieser Qualifizierer erforderlich sind. Optionale Qualifizierer werden in der Spezifikation bereitgestellt, um zufällige benutzerdefinierte Qualifizierer zu vermeiden, die in diesen wiederkehrenden Situationen auftreten können.

<dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Löschen**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Zuordnungen, Verweise

Gibt für Zuordnungen an, ob die qualifizierte Zuordnung gelöscht werden muss, wenn eines der Objekte, auf die in der Zuordnung verwiesen wird, gelöscht wird und ob das entsprechende Objekt, auf das in der Zuordnung verwiesen wird, mit **IfDeleted** qualifiziert ist. Der Standardwert ist **FALSE.**

Für Verweise gibt dieser Qualifizierer an, ob das Objekt, auf das verwiesen wird, gelöscht werden muss, wenn die Zuordnung, die den Verweis enthält, gelöscht und mit **IfDeleted** qualifiziert wird, oder ob eines der Objekte, auf die in der Zuordnung verwiesen wird, gelöscht wird und das entsprechende Objekt, auf das in der Zuordnung verwiesen wird, mit **IfDeleted** qualifiziert wird.

Verwendung: Anwendungen müssen Zuordnungen und Verweise nachverfolgen, die mit dem **Qualifizierer Löschen** markiert sind, und die Zuordnung oder den Verweis entsprechend löschen. Wenn ein Objekt in der Zuordnung gelöscht wurde, aber nicht mit **IfDeleted** markiert ist, sollte die Zuordnung nicht gelöscht werden.

Diese Nutzungsregel muss überprüft werden, wenn das CIM-Sicherheitsmodell definiert ist.

</dd> <dt>

<span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Teuer**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Eigenschaften, Verweise, Klassen, Zuordnungen, Methoden

Gibt an, ob die implizite Aktion umfangreiche Berechnungen erfordert. Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**Wenn gelöscht**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Zuordnungen und Verweise

Gibt an, ob alle Objekte innerhalb einer Zuordnung, die durch **Löschen** qualifiziert ist, gelöscht werden müssen, wenn das Objekt, auf das verwiesen wird, oder die Zuordnung gelöscht wird. Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indizierte**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Eigenschaften, Methoden

Gibt an, ob eine Klasseneigenschaft indiziert werden soll. Bei Anwendung auf Eigenschaften in Klassen, die vom Repository gehostet werden, hat dies nur die Bedeutung, (zum Zeitpunkt der Klassenerstellung) eine schnelle sekundäre Abfragesuche für diese Eigenschaft zu erstellen.

Nur der Wert **TRUE** (Standard) ist zulässig.

</dd> <dt>

<span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Unsichtbar**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Zuordnungen, Eigenschaften, Methoden, Verweise, Klassen

Gibt an, ob die Zuordnung nur für interne Zwecke (z. B. für die Definition der Abhängigkeitssemantik) definiert ist und nicht angezeigt werden soll (z. B. in Zuordnungen). Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Große**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Eigenschaften, Klassen

Gibt an, ob die Eigenschaft oder Klasse eine große Menge an Speicherplatz erfordert. Der Standardwert ist **FALSE.**

</dd> <dt>

<span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Nicht \_ NULL**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: Eigenschaften

Gibt an, ob eine Klasseneigenschaft den Wert **NULL** (**VT \_ NULL**) nicht übernehmen kann. Nur der Wert **TRUE** (Standard) ist zulässig.

Wenn dieser Qualifizierer angegeben ist, lässt WMI die Erstellung von -Instanzen nicht zu, bei denen die -Eigenschaft auf **NULL** festgelegt ist, und **NULL-Eigenschaften** geben den **WBEM \_ E ILLEGAL \_ \_ NULL-Fehlercode** zurück.

Beachten Sie, dass die [**Schlüssel-**](standard-qualifiers.md) und **indizierten** Qualifizierer dieses Verhalten bereits implizieren.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Anbieter**
</dt> <dd>

Datentyp: **string**

Gilt für: Beliebig

Gibt an, dass das Schemaelement dynamisch ist und daher von einem Anbieter aufgefüllt wird. Der Standardwert ist **NULL.** Dieser Qualifizierer ist ein implementierungsspezifisches Handle für die Instrumentierung.

</dd> <dt>

<span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Experimentelle**
</dt> <dd>

Datentyp: **boolescher Wert**

Gilt für: beliebige

Gibt an, dass das angegebene Element als Teil einer zukünftigen Version der CIM-Schemas vorgeschlagen wurde, aber noch nicht Teil des Standardschemas ist. Stattdessen ist das -Element für Benutzer verfügbar, um zu experimentieren, zu implementieren und Feedback zu geben. Basierend auf Feedback kann das Element dem Standard wie dargestellt, geändert oder entfernt hinzugefügt werden. Der Standardwert ist **FALSE.** Eine Implementierung muss kein Element mit diesem Qualifizierer unterstützen.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

Datentyp: **string**

Gilt für: Eigenschaften, Verweise, Methoden, Parameter

Ein bestimmter Typ, der einem Datenelement zugewiesen ist. Der Standardwert ist **NULL.**

Verwendung: Sie müssen den **SyntaxType-Qualifizierer** mit diesem Qualifizierer verwenden.

</dd> <dt>

<span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**
</dt> <dd>

Datentyp: **string**

Gilt für: Eigenschaften, Verweise, Methoden, Parameter

Format des  Syntaxqualifizierers. Der Standardwert ist **NULL.**

Verwendung: Sie müssen den **Syntaxqualifizierer** mit diesem Qualifizierer verwenden.

</dd> <dt>

<span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**
</dt> <dd>

Datentyp: **string**

Gilt für: Klassen, Eigenschaften, Methoden, Zuordnungen, Hinweise, Verweise

Umstände, unter denen ein Trigger ausgelöst wird. Der Standardwert ist **NULL.** Die Triggertypen variieren je nach Metamodellkonstrukt.

Für Klassen und Zuordnungen sind die rechtlichen Werte:

Erstellen

Löschen

Aktualisieren

Zugriff

Für Eigenschaften und Verweise sind die rechtlichen Werte Update und Access.

Bei Methoden sind die rechtlichen Werte Before und After.

Für Hinweise ist der rechtliche Wert Thrown.

</dd> <dt>

<span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Gilt für: Eigenschaften

Ein Satz von Werten, der angibt, dass der Wert der zugeordneten Eigenschaft unbekannt ist (die Eigenschaft kann nicht als gültiger oder sinnvoller Wert betrachtet werden). Der Standardwert ist **NULL.**

Die Konventionen und Einschränkungen, die zum Definieren unbekannter Werte verwendet werden, sind mit denen identisch, die für den [**ValueMap-Qualifizierer**](standard-qualifiers.md) gelten.

Beachten Sie, dass dieser Qualifizierer nicht überschrieben werden kann. Es ist unerklärlich, einer Unterklasse zu erlauben, einen Wert als bekannten Wert zu behandeln, wenn er von einer übergeordneten Klasse als unbekannt behandelt wird.

</dd> <dt>

<span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**
</dt> <dd>

Datentyp: **Zeichenfolgenarray**

Gilt für: Eigenschaften

Ein Satz von Werten, der angibt, dass der Wert der zugeordneten Eigenschaft nicht unterstützt wird (die Eigenschaft kann nicht als gültiger oder sinnvoller Wert betrachtet werden). Der Standardwert ist **NULL.**

Die Konventionen und Einschränkungen, die zum Definieren von nicht unterstützten Werten verwendet werden, sind mit denen identisch, die für den [**ValueMap-Qualifizierer**](standard-qualifiers.md) gelten.

Beachten Sie, dass dieser Qualifizierer nicht überschrieben werden kann. Es ist unerklärlich, einer Unterklasse zu erlauben, einen Wert als unterstützten Wert zu behandeln, der von einer übergeordneten Klasse als unbekannt behandelt wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-Qualifizierer](wmi-qualifiers.md)
</dt> <dt>

[Hinzufügen eines Qualifizierers](adding-a-qualifier.md)
</dt> </dl>

 

 




