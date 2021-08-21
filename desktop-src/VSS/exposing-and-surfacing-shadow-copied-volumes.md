---
description: Zusätzlich zum Zugriff über die IVssBackupComponents-Schnittstelle über das Geräteobjekt seiner Kopie kann ein Anfordernder eine Schattenkopie anderen Prozessen als bereitgestelltes schreibgeschütztes Gerät zur Verfügung stellen.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Verfügbar machen und Schattenkopien von Volumes verfügbar machen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075d22757f5e3bf0bdb81578134d7f0a08ebfb2265edfc4ac8f3d94eecff1a28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938255"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a>Verfügbar machen und Schattenkopien von Volumes verfügbar machen

Zusätzlich zum Zugriff über die [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) über [](vssgloss-d.md)das Geräteobjekt seiner Kopie kann ein An anfordernder Benutzer eine Schattenkopie anderen Prozessen als bereitgestelltes schreibgeschütztes Gerät zur Verfügung stellen.

Dieser Prozess wird als [*Verfügbarstellen*](vssgloss-e.md)einer Schattenkopie bezeichnet und mithilfe der [**IVssBackupComponents::ExposeSnapshot-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) ausgeführt.

Eine Schattenkopie kann als lokales Volume ( einem Laufwerkbuchstaben zugewiesen oder einem bereitgestellten Ordner zugeordnet) oder als Dateifreigabe verfügbar gemacht werden.

Stellen Sie sich zur Veranschaulichung eine Schattenkopie eines Volumes auf dem System vor, die verfügbar gemacht wurdeSys, das in F: bereitgestellt wurde, in dessen Stamm sich die Verzeichnisse dirOne und dirTwo und die Datei \\ FileOne befinden.

## <a name="exposing-a-shadow-copy-locally"></a>Lokales Verfügbarstellen einer Schattenkopie

Bei der Bereitstellung als lokales Volume ist der Stamm der Schattenkopie immer am Bereitstellungspunkt (Laufwerkbuchstaben oder bereitgestellter Ordner) sichtbar, und alle schattenkopierten Dateien sind sichtbar.

Wenn die Schattenkopie lokal über den bereitgestellten Ordner C: ShadowOfF verfügbar gemacht wird, finden Sie alle Dateien, die auf dem Datenträger vorhanden sind, bereitgestellt unter F: zum Zeitpunkt der Schattenkopie unter \\ \\ C: \\ ShadowOfF. Untersuchung von C: ShadowOfF würde zwei Verzeichnisse, dirOne und dirTwo, und eine \\ Datei, fileOne, unter C: \\ ShadowOfF.

Ein Aufruf zum lokalen Verfügbar machen der Schattenkopie kann wie die folgenden sein:

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

Wenn die Schattenkopie lokal erfolgreich verfügbar gemacht wurde, sollte *wszExposed* die Breitzeichenfolge "C: \\ ShadowOfF" enthalten.

Die Schattenkopie kann später durch Aufrufen von [**IVssBackupComponentsEx2::UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot)nicht mehr verfügbar sein.

Nur persistente Schattenkopien , d.> Schattenkopien, die entweder mit VSS \_ CTX NAS ROLLBACK oder \_ \_ VSS CTX APP ROLLBACK erstellt wurden, können \_ lokal verfügbar gemacht \_ \_ werden.

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a>Verfügbar machen einer Schattenkopie als Remotefreigabe

Alternativ können Sie die Schattenkopie des Datenträgers, der in F: bereitgestellt wird, als Remotedateifreigabe verfügbar machen und nur Daten unter dirTwo als Dateifreigabe \\ dirTwoOfF verfügbar machen.

In diesem Fall könnten Systeme auf die Schattenkopie von Dateien unter F: dirTwo zugreifen, indem \\ \\ \\ sie exposedSys \\ dirTwoOfF als Netzwerklaufwerk zuordnen.

Ein Aufruf zum Implementieren der Remote-Offenlegung der Schattenkopie als Freigabe kann folgender sein:

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

Wenn die Schattenkopie erfolgreich remote verfügbar gemacht wurde, sollte *wszExposed* die Breitzeichenfolge "dirTwoOfF" enthalten.

Alle Systeme, die derzeit die Netzwerkfreigabe von dirTwoOfF zuordnen, können die Verbindung mit ihr trennen, so wie es die Verbindung mit jeder normalen Freigabe trennen kann.

## <a name="surfacing-a-shadow-copy"></a>Erstellen einer Schattenkopie

Eine [*surfaced shadow copy ist*](vssgloss-s.md) eine Schattenkopie, in der die Schattenkopie dem Mount Manager-Namespace eines Systems bekannt ist.

Dies bedeutet, dass Sie solche Schattenkopien genau wie alle anderen verfügbaren, aber noch nicht bereitgestellten Volumes finden können, z. B. mit **FindFirstVolume** und **FindNextVolume.**

Offensichtlich handelt es sich bei verfügbar gemachten Schattenkopien also auch um auftdeckte Schattenkopien. Das Gegenteil ist jedoch nicht unbedingt wahr.

Wenn eine lokal verfügbar gemachte Schattenkopie nicht mehr bereitgestellt wird oder ein System eine remote verfügbar gemachte Schattenkopie trennt, wird diese Schattenkopie nicht mehr verfügbar gemacht. Solange die Schattenkopie beibehalten wird, werden die Volumes jedoch angezeigt. Dies bedeutet, dass sie wie jedes andere schreibgeschützte Volume bereitgestellt werden können.

 

 



