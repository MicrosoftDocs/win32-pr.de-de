---
title: version-Attribut
description: Das Attribut \ Version \ Interface identifiziert eine bestimmte Version in mehreren Versionen einer RPC-Schnittstelle. Mit dem Versions Attribut stellen Sie sicher, dass nur kompatible Versionen von Client-und Server Software gebunden werden können.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- Versions Attribut-Mittel l
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacbf7478ebfb745e5fc9b5e50959d0f1587dedf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038014"
---
# <a name="version-attribute"></a>version-Attribut

Das **\[ Versions \]** Schnittstellen Attribut identifiziert eine bestimmte Version in mehreren Versionen einer RPC-Schnittstelle. Mit dem Versions Attribut stellen Sie sicher, dass nur kompatible Versionen von Client-und Server Software gebunden werden können.

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Haupt Wert* 
</dt> <dd>

Gibt eine kurze Ganzzahl ohne Vorzeichen zwischen 0 (null) und 65.535 (einschließlich) an, die die Hauptversionsnummer darstellt.

</dd> <dt>

*nebenwert* 
</dt> <dd>

Gibt eine kurze Ganzzahl ohne Vorzeichen zwischen 0 (null) und 65.535 (einschließlich) an, die die neben Versionsnummer darstellt. Der Wert für die neben Version ist optional. Wenn der Wert vorhanden ist, wird der neben Versions Wert von der Hauptversionsnummer durch ein Zeit Zeichen (.) getrennt. Wenn kein Wert angegeben wird, ist der neben Versions Wert 0 (null).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der mittlerer l-Compiler unterstützt nicht mehrere Versionen einer COM-Schnittstelle. Daher kann eine Schnittstellen Attribut Liste, die das Object-Attribut enthält, **\[** [](object.md) **\]** das **\[ Versions \]** Attribut nicht enthalten. Um eine neue Version einer vorhandenen COM-Schnittstelle zu erstellen, verwenden Sie Schnittstellen Vererbung. Eine abgeleitete com-Schnittstelle hat eine andere UUID, erbt jedoch die Schnittstellen Element Funktionen, Statuscodes und Schnittstellen Attribute der Basisschnittstelle.

In Kombination mit dem **\[** [**UUID**](uuid.md) - **\]** Wert identifiziert der **\[ \] Versions** Wert die-Schnittstelle eindeutig. Die Lauf Zeit Bibliothek übergibt die Werte **\[ Version \]** und **\[ UUID \]** an den Server, wenn der Client eine Remote Funktion aufruft. Ein Client kann für eine bestimmte Schnittstelle eine Bindung an einen Server herstellen, wenn:

-   Der **\[ UUID \]** -Wert ist identisch.
-   Die Hauptversionsnummer ist identisch.
-   Die neben Versionsnummer des Clients ist kleiner oder gleich der neben Versionsnummer des Servers.

Es ist für Sie von Vorteil, und der Vorteil ihrer Benutzer besteht darin, die Kompatibilität der-Schnittstelle zu ändern, sodass nur die neben Versionsnummer geändert wird. Sie können die aufwärts Kompatibilität beibehalten, wenn Sie neue Datentypen hinzufügen, die nicht von vorhandenen Funktionen verwendet werden, und wenn Sie neue Funktionen hinzufügen, ohne die Schnittstellen Spezifikation für vorhandene Funktionen zu ändern.

Ändern Sie die Hauptversionsnummer, wenn eine der folgenden Bedingungen zutrifft:

-   Wenn Sie einen Datentyp ändern, der von einer vorhandenen Funktion verwendet wird.
-   Wenn Sie die Schnittstellen Spezifikation für eine vorhandene Funktion ändern (z. b. hinzufügen oder Entfernen eines Parameters).
-   Wenn Sie Rückrufe hinzufügen, die von vorhandenen Funktionen aufgerufen werden.

Ändern Sie die neben Versionsnummer, wenn alle der folgenden Bedingungen zutreffen:

-   Wenn Sie Typdefinitionen oder Konstanten hinzufügen, die nicht von vorhandenen Funktionen oder Rückrufen verwendet werden.
-   Wenn Sie keine vorhandenen Funktionen ändern und der Schnittstelle neue Funktionen hinzufügen.
-   Wenn Sie Rückrufe hinzufügen, die nicht von vorhandenen Funktionen aufgerufen werden, und die neuen Rückrufe allen vorhandenen Funktionen folgen.

Wenn sich Ihre Änderungen als aufwärts kompatible Änderung an der-Schnittstelle qualifizieren, verwenden Sie das folgende Verfahren.

**So ändern Sie die Schnittstellen Datei (IDL)**

1.  Fügen Sie der Schnittstellen Datei neue Konstanten und Typdefinitionen hinzu.
2.  Fügen Sie Rückruf Funktionen am Ende der Schnittstellen Datei hinzu.
3.  Fügen Sie neue Funktionen am Ende der Schnittstellen Datei hinzu.

Das **\[ Versions \]** Attribut kann höchstens einmal im Schnittstellen Header auftreten.

Wenn das Versions Attribut nicht vorhanden ist, hat die Schnittstelle eine Standardversion von 0,0.

Das Punktzeichen zwischen der Haupt-und der neben Zahl ist ein Trennzeichen, das kein Dezimaltrennzeichen darstellt. Die neben Zahl wird als ganze Zahl behandelt. Führende Nullen sind nicht signifikant. Nachfolgende Nullen sind von Bedeutung.

Beispielsweise stellt die Versions Einstellung 1,11 einen Haupt Wert von einem und einen nebenwert von elf dar. Version 1,11 stellt keinen Wert zwischen 1,1 und 1,2 dar.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**berfläche**](interface.md)
</dt> <dt>

[**Objekt (object)**](object.md)
</dt> <dt>

[**UUID**](uuid.md)
</dt> </dl>

 

 




