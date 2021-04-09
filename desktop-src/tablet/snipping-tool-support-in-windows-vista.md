---
description: In diesem Thema wird beschrieben, wie Ihre Anwendung angeben kann, welche URL das Tablet PC-Snipping-Tool beim Erfassen der Anwendung erhalten soll.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Unterstützung für das Snipping-Tool in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046dd6c8a97d1dacc20065dc1f741610fec13865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867095"
---
# <a name="snipping-tool-support-in-windows-vista"></a>Unterstützung für das Snipping-Tool in Windows Vista

In diesem Thema wird beschrieben, wie Ihre Anwendung angeben kann, welche URL das Tablet PC-Snipping-Tool beim Erfassen der Anwendung erhalten soll.

## <a name="specifying-the-url-via-registry-key"></a>Angeben der URL über den Registrierungsschlüssel

Das Snipping-Tool ermöglicht es Benutzern, ein Ausschnitt (Screenshot) eines beliebigen Objekts auf dem Bildschirm aufzuzeichnen und dann das Image zu kommentieren, zu speichern oder freizugeben. Wenn die Daten im HTML-Format gespeichert werden oder wenn Sie an einen e-Mail-Client gesendet werden, der Inline-HTML unterstützt, kann das Debuggen-Tool dem Ausschnitt eine URL hinzufügen, wenn die Anwendung Informationen zum Abrufen der URL bereitstellt.

Das Snipping-Tool erhält die URL über Barrierefreiheits Objekte. Anwendungen sollten die erforderlichen Informationen unter den folgenden Registrierungs Schlüsseln angeben:

HKLM \\ Software \\ Microsoft \\ Windows \\ TabletPC- \\ Snipping Tool \\ linkfingerabdrücke,

Und sollten einen Unterschlüssel erstellen, dessen Name mit der Fenster Klasse identisch ist, aus der der Link abgerufen werden soll. Der Fenster Klassenname sollte das oberste Fenster der Anwendung sein.

HKLM \\ Software \\ Microsoft \\ Windows \\ TabletPC- \\ Snipping-Tool \\ linkfingerabdrücke\\<Window Class Name>

### <a name="window-class-key-details"></a>Fenster Klassen-Schlüssel Details

Unter dem Fenster Klassen Schlüssel sollten die entsprechenden Werte festgelegt werden, um anzugeben, dass das Erstellungs Tool das richtige Barrierefreiheits Objekt erkennen soll.



| WERT                        | TYPE                  | Chel            | gespeicherte Informationen                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| Mask<br/>              | REG \_ DWORD<br/> |                 | Gibt an, welches der folgenden Felder überprüft werden soll.<br/> |
| Name<br/>              | REG- \_ SZ<br/>    | 0x02<br/> | Name der Barrierefreiheit<br/>                               |
| BESCHREIBUNG<br/>       | REG- \_ SZ<br/>    | 0x04<br/> | Beschreibung der Barrierefreiheit<br/>                        |
| Role<br/>              | REG \_ DWORD<br/> | 0x08<br/> | Barrierefreiheits Rolle<br/>                               |
| ParentName<br/>        | REG- \_ SZ<br/>    | 0x10<br/> | Barrierefreiheits Name des übergeordneten Elements<br/>                     |
| "Parametrivalue"<br/>       | REG- \_ SZ<br/>    | 0x20<br/> | Barrierefreiheits Wert des übergeordneten Elements<br/>                    |
| Element Rolle<br/>        | REG \_ DWORD<br/> | 0x40<br/> | Barrierefreiheits Rolle des übergeordneten Elements<br/>                     |
| Parametridescription<br/> | REG- \_ SZ<br/>    | 0x80<br/> | Barrierefreiheits Beschreibung des übergeordneten Elements<br/>              |



 

Wenn außerdem der Mask-Bitwert 0x1 festgelegt ist, sollte die URL aus dem Barrierefreiheits Namen entnommen werden. Andernfalls sollte die URL aus dem Barrierefreiheits Wert entnommen werden.

Wenn die Anwendung lokalisierte Zeichen folgen für die \_ oben genannten REG SZ-Werte verwendet, sollte die Zeichenfolge im folgenden Format als indirekte Zeichenfolge bereitgestellt werden:

@filename, Ressource

Die Zeichenfolge wird aus der Datei mit dem Namen extrahiert und verwendet dabei den Ressourcen Wert als Locator. Wenn der Ressourcen Wert 0 (null) oder größer ist, wird die Zahl zum Index der Zeichenfolge in der Binärdatei. Wenn die Zahl negativ ist, wird Sie zu einem Ressourcen Bezeichner (ID).

> [!Note]  
> Rollen Konstanten finden Sie in der Windows SDK. Die beschriebenen Registrierungs Werte gelten speziell für Windows Vista.

 

 

 




