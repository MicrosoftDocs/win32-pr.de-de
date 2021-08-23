---
title: Bezeichner für reservierte Eigenschaften
description: Reservierte Eigenschaftenbezeichner können nicht als Eigenschaftenbezeichner (ID) verwendet werden. Jeder Eigenschaftenbezeichner (ID) kann mit Ausnahme von 0, 1 und einem beliebigen Wert verwendet werden, der größer oder gleich 0x80000000. Diese Eigenschaftsbezeichnerwerte sind für die Verwendung durch Anwendungen reserviert.
ms.assetid: d313a7b1-4cac-41f8-ba38-bf9cfaeb9d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05053fd2a31a5e8ceec63420e74884484abef12d44dcfe3e7023c81b5e67e27a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683060"
---
# <a name="reserved-property-identifiers"></a>Bezeichner für reservierte Eigenschaften

Reservierte Eigenschaftenbezeichner können nicht als Eigenschaftenbezeichner (ID) verwendet werden. Jeder Eigenschaftenbezeichner (ID) kann mit Ausnahme von 0, 1 und einem beliebigen Wert verwendet werden, der größer oder gleich 0x80000000. Diese Eigenschaftsbezeichnerwerte sind für die Verwendung durch Anwendungen reserviert.

In der folgenden Tabelle sind die reservierten Eigenschaften-IDs und die Beschreibung der reservierten Eigenschaften-ID aufgeführt.



| RESERVIERTE Eigenschaften-ID | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                    | Für das Erstellen eines optionalen [Eigenschaftensatz-Anzeigenamenwörterbuchs reserviert.](property-set-display-name-dictionary.md) Dies ermöglicht es Eigenschaftensatzbenutzern, Bedeutungen an Eigenschaften anfügen, die über die vom Typindikator bereitgestellten hinausgehen.                                                                                                                                                                                                                                                                                                                                                                |
| 1                    | Reserviert als Indikator für die Codepage (Windows) oder Skript (Macintosh), die beim Interpretieren der Zeichenfolgen im Eigenschaftensatz verwendet werden soll.<br/> Alle Zeichenfolgenwerte im Eigenschaftensatz müssen mit derselben Codepage gespeichert werden. Der ursprüngliche Betriebssystemwert im Eigenschaftensatzheader (PROPERTYSETHEADER::d wOSVer) bestimmt, ob der Codepageindikator einer Windows Codepage oder einem Macintosh-Skript entspricht.<br/>                                                                                                                                                        |
| 0x80000000           | Reserviert als Hinweis auf das Locale, für das der Eigenschaftensatz geschrieben wird.<br/> Das Standard-Locale für einen Eigenschaftensatz ist das Standard-System-Locale (LOCALE \_ SYSTEM \_ DEFAULT). Weitere Informationen zu LOCALE \_ SYSTEM DEFAULT finden Sie in den \_ Win32-APIs. Der Standardwert wird verwendet, wenn der Locale Indicator nicht im Eigenschaftensatz vorhanden ist.<br/>                                                                                                                                                                                                                        |
| 0x80000003           | Reserviert als Indikator für Eigenschaftensatzverhalten. Dieser Eigenschafts-ID-Wert ist eine VT UI4 und beginnt mit einem DWORD-Datentyp, der den Wert VT UI4 enthält, gefolgt von einem DWORD, das das Verhalten des \_  \_ Eigenschaftensets angibt. <br/> Derzeit ist das einzige Bit in diesem Wert, das definiert ist, das bit (0x1). Wenn dieses Bit festgelegt ist, bedeutet dies, dass Namen von Eigenschaftensatznamen, die durch die Eigenschaften-ID 0 angegeben werden, als unter Sensitive Schreibung betrachtet werden sollen. Wenn dieses Bit nicht festgelegt ist oder die Verhaltenseigenschaft (ID 0x80000003) nicht vorhanden ist, sollten die Namen als ohne Unterscheidung nach Groß-/Kleinschreibung betrachtet werden.<br/> |
| 0xFFFFFFFF           | Reserviert für die Benutzerfreundlichkeit der Programmierbarkeit. Es sollte nie in einem serialisierten Eigenschaftensatz angezeigt werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Eigenschaftsbezeichner mit dem hohen Bitsatz (d. h. negativen Werten) sind für die zukünftige Verwendung durch Microsoft reserviert.

Von den reservierten Eigenschaften werden diejenigen mit ID-Werten im Bereich 0x80000000 bis 0xBFFFFFFF von Implementierungen, die ihre Bedeutung nicht verstehen, als schreibgeschützt betrachtet. Wenn eine Implementierung z. B. die Bedeutung von Eigenschafts-0x80000000 nicht versteht, sollte sie zulassen, dass diese Eigenschaft gelesen, aber nicht geschrieben oder gelöscht wird. Eine solche Implementierung sollte es einer Eigenschaft im Bereich 0xC0000000 ermöglichen 0xFFFFFFFE gelesen, geschrieben oder gelöscht werden kann. Die Eigenschafts-ID 0xFFFFFFFF ist ein reservierter Wert und sollte nie in einem serialisierten Eigenschaftensatz angezeigt werden.

## <a name="property-set-locale"></a>Eigenschaftensatz-Locale

Anwendungen können entweder das -Locale unterstützen oder das Standardverhalten verwenden. Es wird empfohlen, dass Anwendungen Benutzern ermöglichen, ein funktionierendes Locale anzugeben. Solche Anwendungen sollten den vom Benutzer angegebenen Locale Identifier in die -Eigenschaft schreiben. Anwendungen, die das Benutzer-Standard-Locale (LOCALE USER DEFAULT) verwenden, sollten \_ \_ den Standard-Locale-Bezeichner des Benutzers in die -Eigenschaft schreiben. Weitere Informationen zu LOCALE \_ USER DEFAULT finden Sie in der \_ Win32-API.

> [!Note]  
> Wenn die [**IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) verwendet wird, um einen Eigenschaftensatz zu erstellen, wird das Standard-Locale des Benutzers automatisch als Locale Indicator geschrieben.

 

Anwendungen sollten auch den Fall eines Fremdobjekts behandeln, bei dem es sich bei dem Locale nicht um das Anwendungs-, Benutzer- oder System-Locale handelt.

Die Locale Indicator-Eigenschaft ist vom Typ VT U14 und besteht daher aus einem DWORD, das VT U14 enthält, gefolgt von einem DWORD mit dem \_ Locale Identifier  (LCID), wie in der \_ Win32-API definiert. 

## <a name="code-page-indicator"></a>Codepageindikator

Wenn eine Anwendung, die nicht der Autor eines Eigenschaftensatz ist, eine Eigenschaft vom Typ Zeichenfolge im Satz ändert, sollte sie den Codepageindikator untersuchen und eine der folgenden Aktionen ausführen:

-   Schreiben Sie die Zeichenfolge in dem vom Codepageindikator angegebenen Format.
-   Ersetzen sie , und schreiben Sie sie erneut, um die Codepage zu ändern.

Wenn eine Anwendung diesen Indikator nicht erkennen kann, sollte sie die -Eigenschaft nicht ändern. Alle Ersteller von Eigenschaftensätzen müssen einen Codepageindikator schreiben. Wenn der Codepageindikator jedoch nicht vorhanden ist, muss von der Codepage auf dem Computer des Lesers ausgegangen werden.

> [!Note]  
> Wenn die [**IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) verwendet wird, um einen Eigenschaftensatz zu erstellen, wird der Codepageindikator automatisch geschrieben.

 

Mögliche Werte für die Codepage finden Sie in der Win32-API (weitere Informationen finden Sie in der [**GetACP-Funktion)**](/windows/desktop/api/winnls/nf-winnls-getacp) und *in Macintosh Volume VI*, Seiten 14-111. (Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.) Beispielsweise wird die Codepage US ANSI durch 0x04E4 (1252 dezimal) dargestellt, während die Codepage für Unicode 0x04B0 (1200 dezimal) ist.

Es wird empfohlen, nach Möglichkeit die Unicode-Codepage zu verwenden und VT LPWSTR anstelle von VT LPSTR zu verwenden, um \_ \_ Multibyte-<->-Unicode-Konvertierungen während des Speicherns und Abrufens zu vermeiden. Die Verwendung derselben Codepage für alle Eigenschaftensätze ist die einzige Möglichkeit, interoperable Eigenschaftensätze weltweit zu erreichen. Beachten Sie auf der Unicode- oder Nicht-Unicode-Codepage, dass die Anzahl am Anfang einer VT LPSTR oder \_ VT BSTR eine \_ **Byteanzahl**  und keine Zeichenanzahl ist. Diese Byteanzahl schließt ein oder zwei 0 Bytes am Ende der Zeichenfolge (das **NULL-Abschlusszeichen** der Zeichenfolge) ein.

Die Eigenschaften-ID 1 ist ein VT I2-Typ und beginnt mit einem DWORD, das den Wert VT I2 gefolgt von einem SHORT-Wert enthält, der die \_  \_ Codepage angibt. 

 

