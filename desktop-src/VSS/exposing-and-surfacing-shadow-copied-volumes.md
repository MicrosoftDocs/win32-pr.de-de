---
description: Zusätzlich zu dem Zugriff über die IVssBackupComponents-Schnittstelle über das Geräte Objekt der Kopie kann ein Anforderer eine Schatten Kopie für andere Prozesse als ein bereitgestelltes Schreib geschütztes Gerät verfügbar machen.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Verfügbar machen und überwinden von schattenkopierten Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353975"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a>Verfügbar machen und überwinden von schattenkopierten Volumes

Zusätzlich zu dem Zugriff über die [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle über das [*Geräte Objekt*](vssgloss-d.md)der Kopie kann ein Anforderer eine Schatten Kopie für andere Prozesse als ein bereitgestelltes Schreib geschütztes Gerät verfügbar machen.

Dieser Prozess wird als verfügbar machen [*einer Schatten Kopie*](vssgloss-e.md)bezeichnet und mithilfe der [**IVssBackupComponents:: exposesnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) -Methode ausgeführt.

Eine Schatten Kopie kann als lokales Volume verfügbar gemacht werden – ein Laufwerk Buchstabe zugewiesen oder einem bereitgestellten Ordner – oder als Dateifreigabe zugeordnet.

Um dies zu veranschaulichen, betrachten Sie eine Schatten Kopie, die auf einem Volume auf dem in F: bereitgestellten System exposedsys enthalten ist \\ .

## <a name="exposing-a-shadow-copy-locally"></a>Lokales verfügbar machen einer Schatten Kopie

Bei der Bereitstellung als lokales Volume wird der Stamm der Schatten Kopie immer am Einfügepunkt (Laufwerk Buchstabe oder eingebundenes Ordner) angezeigt, und alle Dateien mit Schatten Kopie sind sichtbar.

Wenn die Schatten Kopie lokal über den bereitgestellten Ordner C: \\ shadowoff verfügbar gemacht wurde, finden Sie alle Dateien auf dem Datenträger, \\ die zum Zeitpunkt der Bereitstellung von "c: shadowoff" in F: bereitgestellt wurden \\ . Durch die Untersuchung von c: \\ shadowoff werden die beiden Verzeichnisse "dirone" und "dirtwo" und eine Datei ("") unter "c: \\ shadowoff" angezeigt.

Ein lokaler Befehl zum verfügbar machen der Schatten Kopie könnte wie folgt lauten:

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

Wenn die Schatten Kopie erfolgreich lokal verfügbar gemacht wurde, sollte *wszexposed* die breit Zeichen-Zeichenfolge "C: \\ shadowoff" enthalten.

Die Schatten Kopie kann später durch Aufrufen von [**IVssBackupComponentsEx2:: unexposesnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot)nicht verfügbar gemacht werden.

Nur persistente Schatten Kopien – d. h. Schatten Kopien, die entweder mit einem VSS \_ ctx \_ NAS- \_ Rollback oder einem VSS \_ ctx- \_ App-Rollback erstellt wurden \_ – können lokal verfügbar gemacht werden.

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a>Verfügbar machen einer Schatten Kopie als Remote Freigabe

Alternativ dazu können Sie auch festlegen, dass die Schatten Kopie des Datenträgers in F: \\ verfügbar als Remote Dateifreigabe eingebunden werden soll, und dass nur Daten unter dirtwo verfügbar gemacht werden, wenn die Dateifreigabe dirtwooff ist.

In diesem Fall können Systeme auf die Schatten Kopie von Dateien unter F: \\ dirtwo zugreifen, indem Sie \\ \\ exposedsys \\ dirtwooff als Netzwerklaufwerk Mapping.

Ein Befehl zum Implementieren der Remote verfügbar machung der Schatten Kopie als Freigabe könnte wie folgt lauten:

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

Wenn die Schatten Kopie erfolgreich Remote verfügbar gemacht wurde, sollte *wszexposed* die Zeichenfolge "dirtwooff" der breit Zeichenfolge enthalten.

Jedes System, das zurzeit die Netzwerkfreigabe von dirtwooff zuordnet, kann die Verbindung mit dem System trennen, genauso wie es von einer normalen Freigabe getrennt werden kann.

## <a name="surfacing-a-shadow-copy"></a>Sehen Sie sich eine Schatten Kopie an

Eine [*übereinstellungsschattenkopie*](vssgloss-s.md) ist eine, in der die Schatten Kopie dem Mount Manager-Namespace eines Systems bekannt ist.

Dies bedeutet, dass Sie diese Schatten Kopien wie jedes andere verfügbare, aber noch nicht bereitgestellte Volume suchen können – beispielsweise mithilfe von " **findfirstvolume** " und " **findnextvolume**".

Offensichtlich werden auch Schatten Kopien mit dem verfügbar gemachten Schatten kopiert. Das Gegenteil ist jedoch nicht unbedingt der Fall.

Wenn die Bereitstellung einer lokal verfügbar gemachten Schatten Kopie aufgehoben wurde oder ein System die Verbindung mit einer Remote zugänglichen Schatten Kopie getrennt hat, wird diese Schatten Kopie nicht mehr verfügbar gemacht. Solange die Schatten Kopie persistent gespeichert wird, werden die Volumes jedoch angezeigt. Dies bedeutet, dass Sie wie jedes andere schreibgeschützte Volume bereitgestellt werden können.

 

 



