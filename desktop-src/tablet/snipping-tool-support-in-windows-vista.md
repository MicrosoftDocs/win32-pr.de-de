---
description: In diesem Thema wird beschrieben, wie Ihre Anwendung angeben kann, welche URL der Tablet PC-Snipping Tool beim Erfassen Ihrer Anwendung abrufen soll.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Snipping Tool-Unterstützung in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb2c24901524500df97461f3b3acf88d9a51f73cc24134955c1df866a457a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966769"
---
# <a name="snipping-tool-support-in-windows-vista"></a>Snipping Tool-Unterstützung in Windows Vista

In diesem Thema wird beschrieben, wie Ihre Anwendung angeben kann, welche URL der Tablet PC-Snipping Tool beim Erfassen Ihrer Anwendung abrufen soll.

## <a name="specifying-the-url-via-registry-key"></a>Angeben der URL über den Registrierungsschlüssel

Snipping Tool können Benutzer einen Snip (Screenshot) eines beliebigen Objekts auf dem Bildschirm erfassen und dann das Bild kommentieren, speichern oder freigeben. Wenn die Daten im HTML-Format gespeichert oder an einen E-Mail-Client gesendet werden, der Inline-HTML unterstützt, kann Snipping Tool dem Snip eine URL hinzufügen, wenn die Anwendung Informationen zum Abrufen der URL enthält.

Snipping Tool die URL über Barrierefreiheitsobjekte. Anwendungen sollten die erforderlichen Informationen unter den folgenden Registrierungsschlüsseln angeben:

HKLM \\ Software Microsoft Windows \\ \\ \\ TabletPC Snipping Tool \\ \\ LinkFingerprints,

Und sollte einen Unterschlüssel erstellen, dessen Name mit der Fensterklasse identisch ist, aus der der Link erhalten werden soll. Der Name der Fensterklasse sollte das oberste Fenster der Anwendung sein.

HKLM \\ Software Microsoft Windows \\ \\ \\ TabletPC Snipping Tool \\ \\ LinkFingerprints\\<Window Class Name>

### <a name="window-class-key-details"></a>Schlüsseldetails der Window-Klasse

Unter dem Fensterklassenschlüssel sollten die entsprechenden Werte festgelegt werden, um anzugeben, Snipping Tool das richtige Barrierefreiheitsobjekt erkennen soll.



| WERT                        | TYPE                  | Maske            | GESPEICHERTE INFORMATIONEN                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| Mask<br/>              | REG \_ DWORD<br/> |                 | Gibt an, welches der folgenden Felder überprüft werden soll.<br/> |
| Name<br/>              | REG \_ SZ<br/>    | 0x02<br/> | Name der Barrierefreiheit<br/>                               |
| Beschreibung<br/>       | REG \_ SZ<br/>    | 0x04<br/> | Beschreibung der Barrierefreiheit<br/>                        |
| Rolle<br/>              | REG \_ DWORD<br/> | 0x08<br/> | Barrierefreiheitsrolle<br/>                               |
| ParentName<br/>        | REG \_ SZ<br/>    | 0x10<br/> | Barrierefreiheitsname des übergeordneten Elements<br/>                     |
| ParentValue<br/>       | REG \_ SZ<br/>    | 0x20<br/> | Barrierefreiheitswert des übergeordneten Elements<br/>                    |
| ParentRole<br/>        | REG \_ DWORD<br/> | 0x40<br/> | Barrierefreiheitsrolle des übergeordneten Elements<br/>                     |
| ParentDescription<br/> | REG \_ SZ<br/>    | 0x80<br/> | Beschreibung der Barrierefreiheit des übergeordneten Elements<br/>              |



 

Wenn außerdem der Maskenbitwert 0x1 festgelegt ist, sollte die URL aus dem Namen der Barrierefreiheit übernommen werden. Andernfalls sollte die URL aus dem Barrierefreiheitswert übernommen werden.

Wenn die Anwendung lokalisierte Zeichenfolgen für die oben genannten REG SZ-Werte verwendet, sollte die Zeichenfolge als indirekte Zeichenfolge im \_ folgenden Format bereitgestellt werden:

@filenameRessource

Die Zeichenfolge wird aus der Datei mit dem Namen extrahiert, indem der Ressourcenwert als Locator verwendet wird. Wenn der Ressourcenwert 0 (null) oder größer ist, wird die Zahl zum Index der Zeichenfolge in der Binärdatei. Wenn die Zahl negativ ist, wird sie zu einem Ressourcenbezeichner (ID).

> [!Note]  
> Rollenkonst constants finden Sie in oleacc.h im Windows SDK. Die beschriebenen Registrierungswerte gelten speziell für Windows Vista.

 

 

 




