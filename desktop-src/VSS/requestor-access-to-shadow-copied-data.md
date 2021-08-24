---
description: Sobald die Schattenkopie abgeschlossen ist, ist der wichtigste Mechanismus für den Zugriff auf die dateidaten, die sie enthält, die Verwendung des Geräteobjekts der Schattenkopie.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Zugriff des An anfordernden Auf Schattenkopien von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779e3947adff28c8f3190026921c398677afc7efaa484903bf165250f41bc191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767700"
---
# <a name="requester-access-to-shadow-copied-data"></a>Zugriff des An anfordernden Auf Schattenkopien von Daten

Sobald die Schattenkopie abgeschlossen ist, ist der wichtigste Mechanismus für den Zugriff auf die dateidaten, die sie enthält, die Verwendung des Geräteobjekts der [*Schattenkopie.*](vssgloss-d.md)

Das **m \_ pwszSnapshotDeviceObject-Member** einer [**VSS SNAPSHOT \_ \_ PROP-Struktur**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ist eine Zeichenfolge, die das Geräteobjekt eines kopierten Volumes enthält. Ein Anfordernder kann das **VSS \_ SNAPSHOT \_ PROP-Objekt** eines schattenkopierten Volumes abrufen, wenn er die **VSS-ID \_** des Volumes (identifizierende GUID) kennt und es [**an IVssBackupComponents::GetSnapshotProperties übergibt.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)

Ein Anfrager kann auch Schattenkopie-Eigenschaftsinformationen abrufen, indem er das **Obj.Snap-Member** der [**VSS \_ OBJECT \_ PROP-Struktur**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (eine [**VSS \_ SNAPSHOT \_ PROP-Struktur)**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) verwendet, die mithilfe von [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) ermittelt wurde, um die Liste der Objekte zu iterieren, die durch einen Aufruf von [**IVssBackupComponents::Query zurückgegeben werden.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)

Das Geräteobjekt sollte als Stamm eines Schattenkopie-Volumes interpretiert werden. Aus diesem Grund enthält das Geräteobjekt keinen zurücken Schrägstrich (" \\ ").

Pfade auf dem kopierten Schattenvolumen werden durch Ersetzen des Stamms des ursprünglichen Pfads durch das Geräteobjekt ermittelt. Wenn Sie beispielsweise einen Pfad auf dem ursprünglichen Volume von "C: DATABASE .mdb" und einer VSS SNAPSHOT PROP-Instanz von snapProp erhalten, erhalten Sie den Pfad auf dem kopierten Schattenvolumen, indem Sie \\ \\ \* snapPropm [**\_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) \_ pwszShadow copyDeviceObject, " \\ ", und " \\ DATABASE \\ \* .mdb" verketten.

Die VSS-Dateisätze enthalten möglicherweise Platzhalterzeichen in ihren Dateideskriptoren, sodass das Abrufen einer vollständigen Liste der Dateien auf einer Schattenkopie, die von einer Komponente verwaltet wird, möglicherweise die Verwendung von Methoden wie **FindFileFirst,** **FindFileFirstEx** und **FindNextFile erfordert.**

 

 



