---
title: version-Attribut
description: Das Schnittstellenattribut \version\identifiziert eine bestimmte Version unter mehreren Versionen einer RPC-Schnittstelle. Mit dem Versionsattribut stellen Sie sicher, dass nur kompatible Versionen der Client- und Serversoftware gebunden werden dürfen.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- Versionsattribut MIDL
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c72cc825183740d856c20b9e5c76ece472f82db405d9560e6502f6e32985b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252110"
---
# <a name="version-attribute"></a>version-Attribut

Das **\[ \] Versionsschnittstellenattribut** identifiziert eine bestimmte Version unter mehreren Versionen einer RPC-Schnittstelle. Mit dem Versionsattribut stellen Sie sicher, dass nur kompatible Versionen der Client- und Serversoftware gebunden werden dürfen.

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Hauptwert* 
</dt> <dd>

Gibt eine kurze ganze Zahl ohne Vorzeichen zwischen 0 (null) und 65.535 (einschließlich) an, die die Hauptversionsnummer darstellt.

</dd> <dt>

*Nebenwert* 
</dt> <dd>

Gibt eine kurze ganze Zahl ohne Vorzeichen zwischen 0 (null) und 65.535 (einschließlich) an, die die Nebenversionsnummer darstellt. Der Nebenversionswert ist optional. Falls vorhanden, wird der Nebenversionswert durch ein Zeichen (.) von der Hauptversionsnummer getrennt. Wenn kein Wert angegeben wird, ist der Nebenversionswert 0 (null).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der MIDL-Compiler unterstützt nicht mehrere Versionen einer COM-Schnittstelle. Daher kann eine Schnittstellenattributliste, die das **\[** [**Objektattribut**](object.md) **\]** enthält, das **\[ Versionsattribut \] nicht** enthalten. Verwenden Sie schnittstellenvererbung, um eine neue Version einer vorhandenen COM-Schnittstelle zu erstellen. Eine abgeleitete COM-Schnittstelle verfügt über eine andere UUID, erbt jedoch die Schnittstellenmitgliedsfunktionen, Statuscodes und Schnittstellenattribute der Basisschnittstelle.

In Kombination mit dem **\[** [**uuid-Wert**](uuid.md) **\]** identifiziert der **\[ Versionswert \]** die Schnittstelle eindeutig. Die Laufzeitbibliothek übergibt die **\[ Versions- und \]** **\[ uuid-Werte \]** an den Server, wenn der Client eine Remotefunktion aufruft. Ein Client kann eine Bindung an einen Server für eine bestimmte Schnittstelle herstellen, wenn:

-   Der **\[ uuid-Wert \]** ist identisch.
-   Die Hauptversionsnummer ist identisch.
-   Die Nebenversionsnummer des Clients ist kleiner oder gleich der Nebenversionsnummer des Servers.

Es ist zu Ihrem Vorteil und dem Vorteil Ihrer Benutzer, die Aufwärtskompatibilität zwischen den Versionen auf dem neuesten Stand zu halten, d. b. die Schnittstelle so zu ändern, dass sich nur die Nebenversionsnummer ändert. Sie können die Aufwärtskompatibilität beibehalten, wenn Sie neue Datentypen hinzufügen, die nicht von vorhandenen Funktionen verwendet werden, und wenn Sie neue Funktionen hinzufügen, ohne die Schnittstellenspezifikation für vorhandene Funktionen zu ändern.

Ändern Sie die Hauptversionsnummer, wenn eine der folgenden Bedingungen zu erfüllen ist:

-   Wenn Sie einen Datentyp ändern, der von einer vorhandenen Funktion verwendet wird.
-   Wenn Sie die Schnittstellenspezifikation für eine vorhandene Funktion ändern (z. B. Hinzufügen oder Entfernen eines Parameters).
-   Wenn Sie Rückrufe hinzufügen, die von vorhandenen Funktionen aufgerufen werden.

Ändern Sie die Nebenversionsnummer, wenn alle der folgenden Bedingungen erfüllt sind:

-   Wenn Sie Typdefinitionen oder Konstanten hinzufügen, die nicht von vorhandenen Funktionen oder Rückrufen verwendet werden.
-   Wenn Sie keine vorhandenen Funktionen ändern und der Schnittstelle neue Funktionen hinzufügen.
-   Wenn Sie Rückrufe hinzufügen, die nicht von vorhandenen Funktionen aufgerufen werden, folgen die neuen Rückrufe allen vorhandenen Funktionen.

Wenn Ihre Änderungen als aufwärtskompatible Änderung an der Schnittstelle gelten, gehen Sie wie folgt vor.

**So ändern Sie die Schnittstellendatei (IDL)**

1.  Fügen Sie der Schnittstellendatei neue Konstanten- und Typdefinitionen hinzu.
2.  Fügen Sie Rückruffunktionen am Ende der Schnittstellendatei hinzu.
3.  Fügen Sie am Ende der Schnittstellendatei neue Funktionen hinzu.

Das **\[ \] Versionsattribut** kann im Schnittstellenheader mindestens einmal auftreten.

Wenn das Versionsattribut nicht vorhanden ist, verfügt die Schnittstelle über die Standardversion 0.0.

Das Punktzeichen zwischen den Haupt- und Nebenzahlen ist ein Trennzeichen und stellt kein Dezimaltrennzeichen dar. Die Nebenzahl wird als ganze Zahl behandelt. Führende Nullen sind nicht signifikant. Nach trailende Nullen sind von Bedeutung.

Beispielsweise stellt die Versionseinstellung 1.11 einen Hauptwert von eins und einen Nebenwert von elf dar. Version 1.11 stellt keinen Wert zwischen 1.1 und 1.2 dar.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Schnittstelle**](interface.md)
</dt> <dt>

[**Objekt (object)**](object.md)
</dt> <dt>

[**Uuid**](uuid.md)
</dt> </dl>

 

 




