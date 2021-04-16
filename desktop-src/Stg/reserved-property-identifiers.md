---
title: Reservierte Eigenschaften Bezeichner
description: Reservierte Eigenschaften Bezeichner können nicht als Eigenschaften Bezeichner (ID) verwendet werden. Alle Eigenschaften Bezeichner (ID) können mit Ausnahme von 0, 1 und einem beliebigen Wert größer oder gleich 0x80000000 verwendet werden. Diese eigenschaftenbezeichnerwerte sind für die Verwendung durch Anwendungen reserviert.
ms.assetid: d313a7b1-4cac-41f8-ba38-bf9cfaeb9d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a16a8e232a31864a402b01033a829183105905c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473285"
---
# <a name="reserved-property-identifiers"></a>Reservierte Eigenschaften Bezeichner

Reservierte Eigenschaften Bezeichner können nicht als Eigenschaften Bezeichner (ID) verwendet werden. Alle Eigenschaften Bezeichner (ID) können mit Ausnahme von 0, 1 und einem beliebigen Wert größer oder gleich 0x80000000 verwendet werden. Diese eigenschaftenbezeichnerwerte sind für die Verwendung durch Anwendungen reserviert.

In der folgenden Tabelle werden die reservierten Eigenschaften-IDs und die Beschreibung der reservierten Eigenschaften-ID aufgelistet.



| Reservierte Eigenschaften-ID | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                    | Reserviert zum Erstellen eines optionalen [Eigenschaften Satz-Anzeige namens Wörterbuch](property-set-display-name-dictionary.md). Dadurch können Benutzer von Eigenschaften Gruppen die Bedeutung an Eigenschaften anfügen, über diejenigen hinaus, die vom Typindikator bereitgestellt werden.                                                                                                                                                                                                                                                                                                                                                                |
| 1                    | Wird als Indikator der Codepage (Windows) oder des Skripts (Macintosh) reserviert, das beim Interpretieren der Zeichen folgen im Eigenschaften Satz verwendet werden soll.<br/> Alle Zeichen folgen Werte im Eigenschaften Satz müssen mit der gleichen Codepage gespeichert werden. Der Wert des Ursprungs Betriebssystems im Eigenschaften Satz Header (propertyseteader::d wosver) bestimmt, ob der Code Page Indikator einer Windows-Codepage oder einem Macintosh-Skript entspricht.<br/>                                                                                                                                                        |
| 0x80000000           | Reserviert als Angabe des Gebiets Schemas, für das der Eigenschaften Satz geschrieben wird.<br/> Das Standard Gebiets Schema für einen Eigenschaften Satz ist das Standard Gebiets Schema des Systems (locale \_ System \_ Default). Weitere Informationen zum standardmäßigen Gebiets Schema \_ System finden Sie in \_ den Win32-APIs. Der Standardwert wird verwendet, wenn der Gebiets Schema Indikator im Eigenschaften Satz nicht vorhanden ist.<br/>                                                                                                                                                                                                                        |
| 0x80000003           | Reserviert als Indikator für Eigenschaften Satz Verhalten. Dieser Eigenschafts-ID-Wert ist ein VT \_ -UI4 und beginnt mit einem **DWORD** -Datentyp, der den Wert VT \_ UI4, gefolgt von einem **DWORD** , das Eigenschaften Satz Verhalten angibt.<br/> Derzeit ist das einzige Bit in diesem Wert, das definiert ist, das Bit mit niedriger Ordnung (0x1). Wenn dieses Bit festgelegt ist, gibt es an, dass durch die Eigenschaften-ID 0 angezeigtes Eigenschafts Satz Namen bei der Groß-/Kleinschreibung beachtet werden Wenn dieses Bit nicht festgelegt ist oder die Behavior-Eigenschaft (ID 0x80000003) nicht vorhanden ist, sollten die Namen bei der Groß-/Kleinschreibung nicht beachtet werden.<br/> |
| 0xFFFFFFFF           | Reserviert für die einfache Programmierbarkeit. Sie darf nie in einem serialisierten Eigenschaften Satz enthalten sein.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Eigenschafts Bezeichner mit dem High-Bit-Satz (d. h. negative Werte) sind für die zukünftige Verwendung durch Microsoft reserviert.

Von den reservierten Eigenschaften werden diejenigen mit ID-Werten im Bereich 0x80000000 bis 0xBFFFFFFF von Implementierungen als schreibgeschützt betrachtet, die ihre Bedeutung nicht verstehen. Wenn eine Implementierung z. b. die Bedeutung der Eigenschaft 0x80000000 nicht versteht, sollte Sie zulassen, dass diese Eigenschaft gelesen, jedoch nicht geschrieben oder gelöscht wird. Eine solche Implementierung sollte es ermöglichen, dass eine Eigenschaft im Bereich 0xC0000000 auf 0xFFFFFFFE gelesen, geschrieben oder gelöscht wird. Die eigen schafts-ID 0xFFFFFFFF ist ein reservierter Wert und sollte nie in einem serialisierten Eigenschaften Satz enthalten sein.

## <a name="property-set-locale"></a>Gebiets Schema für Eigenschaften Satz

Anwendungen können auswählen, ob das Gebiets Schema unterstützt oder das Standardverhalten verwendet werden soll. Es wird empfohlen, dass Anwendungen Benutzern gestatten, ein funktionierendes Gebiets Schema anzugeben. Solche Anwendungen sollten den vom Benutzer angegebenen Gebiets Schema Bezeichner in die-Eigenschaft schreiben. Anwendungen, die das Standard Gebiets Schema des Benutzers verwenden (locale \_ User \_ Default), sollten den Benutzer standardgebiets Schema Bezeichner in die Eigenschaft schreiben. Weitere Informationen zum \_ \_ Standardbenutzer Standard finden Sie in der Win32-API.

> [!Note]  
> Wenn die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle verwendet wird, um einen Eigenschaften Satz zu erstellen, wird das Standard Gebiets Schema des Benutzers automatisch als Gebiets Schema Indikator geschrieben.

 

Anwendungen sollten auch die Groß-/Kleinschreibung eines fremden Objekts behandeln, bei dem es sich nicht um das Anwendungs Gebiets Schema, das Gebiets Schema des Benutzers oder das Gebiets Schema des Systems handelt.

Die Gebiets Schema Indikator Eigenschaft hat den Typ VT \_ U14 und besteht daher aus einem **DWORD** , das VT \_ U14 enthält, gefolgt von einem **DWORD** , das den Gebiets Schema Bezeichner (LCID) enthält, wie in der Win32-API definiert.

## <a name="code-page-indicator"></a>Code Page Indikator

Wenn eine Anwendung, die nicht der Autor eines Eigenschafts Satzes ist, eine Eigenschaft vom Typ Zeichenfolge im Satz ändert, sollte Sie den Code Page Indikator überprüfen und eine der folgenden Aktionen ausführen:

-   Schreiben Sie die Zeichenfolge in dem vom Code Page Indikator angegebenen Format.
-   Ersetzen und umschreiben, um die Codepage zu ändern.

Wenn eine Anwendung diesen Indikator nicht erkennen kann, sollte die Eigenschaft nicht geändert werden. Alle Ersteller von Eigenschafts Sätzen müssen einen Code Page Indikator schreiben. Wenn der Code Page Indikator jedoch nicht vorhanden ist, muss die vorherrschende Codepage auf dem Computer des Readers angenommen werden.

> [!Note]  
> Wenn die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle verwendet wird, um einen Eigenschaften Satz zu erstellen, wird der Code Page Indikator automatisch geschrieben.

 

Mögliche Werte für die Codepage sind in der Win32-API angegeben (Weitere Informationen finden Sie unter der [**GetACP**](/windows/desktop/api/winnls/nf-winnls-getacp) -Funktion) und *in Macintosh Volume VI*, Pages 14-111. (Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.) Beispielsweise wird die Codepage US ANSI durch 0x04e4 (1252 in dezimal) dargestellt, während die Codepage für Unicode 0x04b0 (1200 in Decimal) ist.

Es wird empfohlen, nach Möglichkeit die Unicode-Codepage zu verwenden und VT \_ LPWSTR anstelle von VT \_ LPSTR zu verwenden, um beim Speichern und Abrufen Multibytezeichen-< > Unicode-Konvertierungen zu vermeiden. Die Verwendung derselben Codepage für alle Eigenschaften Sätze ist die einzige Möglichkeit, interoperable Eigenschaften Sätze auf der ganzen Welt zu erreichen. Beachten Sie in der Codepage Unicode oder nicht-Unicode, dass die Anzahl am Anfang eines VT \_ LPSTR oder VT \_ BSTR eine **Byte** Anzahl und keine **Zeichen** Anzahl ist. Diese Byte Anzahl schließt die 1 oder zwei 0 Bytes am Ende der Zeichenfolge ein (das **null** -Terminator der Zeichenfolge).

Die eigen schafts-ID 1 ist ein VT \_ I2 Type und beginnt mit einem **DWORD** , das den Wert VT \_ I2 gefolgt von einem **kurzen** , der die Codepage angibt, enthält.

 

