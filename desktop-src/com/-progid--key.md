---
title: ProgID-Schlüssel
description: Eine programmgesteuerte Kennung (ProgID) ist ein Registrierungs Eintrag, der einer CLSID zugeordnet werden kann. Wie die CLSID identifiziert die ProgID eine Klasse, jedoch mit geringerer Genauigkeit, da Sie nicht unbedingt global eindeutig ist.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039974"
---
# <a name="progid-key"></a>ProgID-Schlüssel

Eine programmgesteuerte Kennung (ProgID) ist ein Registrierungs Eintrag, der einer CLSID zugeordnet werden kann. Wie die CLSID identifiziert die ProgID eine Klasse, jedoch mit geringerer Genauigkeit, da Sie nicht unbedingt global eindeutig ist.

## <a name="registry-entry"></a>Registrierungseintrag

**HKEY \_ \_ \\ Software \\ Klassen des lokalen** Computers \\ *{* ProgID *}*



| Registrierungsschlüssel                            | Beschreibung                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [**CLSID**](clsid.md)                  | Ordnet eine ProgID einer CLSID zu.                                  |
| [**Einfügbar**](insertable-progid.md) | Gibt an, dass diese Klasse in OLE 2-Containern einfügbar ist.       |
| [**Protokoll**](protocol.md)            | Gibt an, dass diese OLE 2-Klasse in OLE 1-Containern einfügbar ist. |
| [**Shell**](shell.md)                  | Bietet Informationen zum Drucken von Windows 3,1-Shell und zum **Öffnen von Dateien** . |



 

## <a name="remarks"></a>Bemerkungen

Eine ProgID kann in Programmier Situationen verwendet werden, in denen eine CLSID nicht verwendet werden kann. ProgIDs sollten nicht in der Benutzeroberfläche angezeigt werden. ProgIDs sind nicht garantiert eindeutig und können daher nur verwendet werden, wenn Namenskonflikte verwaltbar sind.

Das Format einer ProgID ist <*Programm*>. <*Component*>. <*Version*>, getrennt durch Punkte und ohne Leerzeichen, wie in Word.Doc"beent. 6". Die ProgID muss die folgenden Anforderungen erfüllen:

-   Es sind nicht mehr als 39 Zeichen vorhanden.
-   Enthalten keine Interpunktions Zeichen (einschließlich Unterstriche), mit Ausnahme von mindestens einem Zeitraum.
-   Beginnen Sie nicht mit einer Ziffer.
-   Unterscheiden Sie sich vom Klassennamen jeder OLE 1-Anwendung, einschließlich der OLE 1-Version der gleichen Anwendung (sofern vorhanden).

Da die ProgID nicht in der Benutzeroberfläche angezeigt werden sollte, können Sie einen anzeigbaren Namen abrufen, indem Sie [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)aufrufen. Siehe auch [**olereggetusertype**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).

Der Schlüssel **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** entspricht dem Stamm Schlüssel der **HKEY- \_ Klassen \_** , der für die Kompatibilität mit früheren Versionen von com beibehalten wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[**Olereggetusertype**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




