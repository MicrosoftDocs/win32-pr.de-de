---
description: Die folgende Schnittstellen Definition wird als Standard bereitgestellt, der bei der Entwicklung eines Smartcard-Dienstanbieters befolgt werden kann.
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: Iscardfileaccess-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866259"
---
# <a name="iscardfileaccess-interface"></a>Iscardfileaccess-Schnittstelle

\[Die **iscardfileaccess** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die folgende Schnittstellen Definition wird als Standard bereitgestellt, der bei der Entwicklung eines [*Smartcard*](../secgloss/s-gly.md) - [*Dienstanbieters*](../secgloss/c-gly.md)befolgt werden kann.

Die **iscardfileaccess** -Schnittstelle kann verwendet werden, um eine allgemeine Schnittstelle für ein Karten basiertes Dateisystem mit einem zugrunde liegenden Kartendatei System zu implementieren, das auf der Struktur basiert, die in ISO/IEC 7816-4 definiert ist. Andere Implementierungen sind möglich, dies ist jedoch erwartungsgemäß die häufigste.

Die **iscardfileaccess** -Schnittstelle kann verwendet werden, um Dateisystem Entitäten auf eine Weise verfügbar zu machen, die Anwendungsentwicklern in der PC-Umgebung sehr vertraut ist. Es stellt Mechanismen bereit, um bestimmte Dateien zu suchen und allgemeine Vorgänge auszuführen, z. b. das auswählen, lesen, schreiben, erstellen und löschen. Es kapselt und maskiert einen Großteil der Details auf niedriger Ebene, die an der Ausführung dieser Vorgänge auf Kartenebene beteiligt sind.

Im folgenden finden Sie eine typische Verwendung der **iscardfileaccess** -Schnittstelle. In diesem Fall wird die **iscardfileaccess** -Schnittstelle verwendet, um eine Datei auszuwählen, zu öffnen und in eine Datei zu schreiben.

**So schreiben Sie in eine Datei**

1.  Rufen Sie [**iscardmanage:: kreatefileaccess**](iscardmanage-createfileaccess.md) auf, um eine **iscardfileaccess** -Schnittstelle zu erstellen.
2.  [**Öffnen Sie öffnen**](iscardfileaccess-open.md) , um die Datei auszuwählen und zu öffnen.
3.  Ruft [**Schreib**](iscardfileaccess-write.md)Vorgänge auf.
4.  [**Schließen**](iscardfileaccess-close.md)Sie den Befehl.
5.  Geben Sie die **iscardfileaccess** -Schnittstelle frei.

## <a name="members"></a>Member

Die **iscardfileaccess** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscardfileaccess** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iscardfileaccess** -Schnittstelle verfügt über diese Methoden.



| Methode                                                              | BESCHREIBUNG                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Changedir**](iscardfileaccess-changedir.md)                     | Ändert das aktuelle Smartcardverzeichnis in das neue angegebene Verzeichnis.<br/>                                                          |
| [**Schließen**](iscardfileaccess-close.md)                             | Schließt die angegebene Datei.<br/>                                                                                                        |
| [**Stelle**](iscardfileaccess-create.md)                           | Erstellt eine Datei an einem bestimmten Speicherort im Dateisystem des Dateisystems.<br/>                                                                    |
| [**Lösch**](iscardfileaccess-delete.md)                           | Löscht eine angegebene Datei.<br/>                                                                                                         |
| [**Verzeichnis**](iscardfileaccess-directory.md)                     | Ruft eine Liste der Dateien ab.<br/>                                                                                                        |
| [**Getcurrentdir**](iscardfileaccess-getcurrentdir.md)             | Gibt einen absoluten Pfad zum aktuell ausgewählten Verzeichnis zurück.<br/>                                                                     |
| [**Getfilefunktionen**](iscardfileaccess-getfilecapabilities.md) | Ruft Dateifunktionen ab.<br/>                                                                                                      |
| [**GetProperties**](iscardfileaccess-getproperties.md)             | Ruft die primitiven Daten ab, auf die von Tags für das angegebene Objekt verwiesen wird.<br/>                                                           |
| [**Ungültig**](iscardfileaccess-invalidate.md)                   | Legt fest, dass die angegebene Datei ungültig ist.<br/>                                                                                               |
| [**Eren**](iscardfileaccess-open.md)                               | Öffnet die angegebene Datei zur weiteren Verwendung.<br/>                                                                                         |
| [**Lesen**](iscardfileaccess-read.md)                               | Liest die angegebenen Daten aus einer angegebenen Datei und gibt Sie zurück.<br/>                                                                           |
| [**Rehabilitations**](iscardfileaccess-rehabilitate.md)               | Erstellt eine Datei (EF oder DF), die zuvor mit dem Befehl Invalidate, der für die Anwendung zugänglich ist, nicht gültig ist.<br/> |
| [**Seek**](iscardfileaccess-seek.md)                               | Wählt das Objekt aus, von dem die Lese-/Schreibberechtigung ausgeführt wird.<br/>                                                                 |
| [**SetProperties**](iscardfileaccess-setproperties.md)             | Legt die primitiven Daten fest, auf die von Tags für das angegebene Objekt verwiesen wird.<br/>                                                                |
| [**Schreiben**](iscardfileaccess-write.md)                             | Schreibt Daten in eine aktuelle geöffnete Datei.<br/>                                                                                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



 

 
