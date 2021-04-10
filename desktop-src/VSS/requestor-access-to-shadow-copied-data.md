---
description: Wenn die Schatten Kopie abgeschlossen ist, ist der wichtigste Mechanismus für den Zugriff auf die darin enthaltenen Datei Daten die Verwendung des Geräte Objekts der Schatten Kopie.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Zugriff auf Schatten Kopien von Daten Anforderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6265586f70054277170b44f23efc52d56842e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131265"
---
# <a name="requester-access-to-shadow-copied-data"></a><span data-ttu-id="55033-103">Zugriff auf Schatten Kopien von Daten Anforderer</span><span class="sxs-lookup"><span data-stu-id="55033-103">Requester Access to Shadow Copied Data</span></span>

<span data-ttu-id="55033-104">Wenn die Schatten Kopie abgeschlossen ist, ist der wichtigste Mechanismus für den Zugriff auf die darin enthaltenen Datei Daten die Verwendung des [*Geräte Objekts*](vssgloss-d.md)der Schatten Kopie.</span><span class="sxs-lookup"><span data-stu-id="55033-104">Once the shadow copy has completed, the most important mechanism for getting access to the file data it contains is through the use of the shadow copy's [*device object*](vssgloss-d.md).</span></span>

<span data-ttu-id="55033-105">Der **m \_ pwszsnapshotdeviceobject** -Member einer [**VSS \_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) -momentaufnahmenstruktur ist eine Zeichenfolge, die das Geräte Objekt eines schattenkopierten Volumes enthält.</span><span class="sxs-lookup"><span data-stu-id="55033-105">The **m\_pwszSnapshotDeviceObject** member of a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure is a string containing a shadow-copied volume's device object.</span></span> <span data-ttu-id="55033-106">Ein Anforderer kann das **VSS \_ Snapshot \_ Prop** -Objekt eines schattenkopierten Volumes abrufen, wenn es die **VSS- \_ ID** des Volumes kennt (Identifikations-GUID), und es an [**IVssBackupComponents:: getionnapshotproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)übergibt.</span><span class="sxs-lookup"><span data-stu-id="55033-106">A requester can obtain a shadow-copied volume's **VSS\_SNAPSHOT\_PROP** object if it knows the volume's **VSS\_ID** (identifying GUID) and passes it to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="55033-107">Ein Anforderer kann mithilfe des **obj. Snap** -Members der [**VSS- \_ Objekt- \_ Prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) -Struktur (bei der es sich um eine [**VSS \_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) -momentaufnahmenstruktur handelt) auch Informationen über die Eigenschaften der Schatten Kopie [**abrufen, um**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) die Liste der Objekte zu durchlaufen, die durch einen-Befehl von [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="55033-107">A requester can also obtain shadow copy property information by using the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) structure (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

<span data-ttu-id="55033-108">Das Geräte Objekt sollte als Stamm eines schattenkopierten Volumes interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="55033-108">The device object should be interpreted as the root of a shadow-copied volume.</span></span> <span data-ttu-id="55033-109">Aus diesem Grund enthält das Device-Objekt keinen umgekehrten Schrägstrich (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="55033-109">For this reason, the device object contains no backslash ("\\").</span></span>

<span data-ttu-id="55033-110">Pfade im schattenkopierten Volume werden abgerufen, indem der Stamm des ursprünglichen Pfads durch das Geräte Objekt ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="55033-110">Paths on the shadow copied volume are obtained by replacing the root of the original path with the device object.</span></span> <span data-ttu-id="55033-111">Wenn Sie z. b. einen Pfad zum ursprünglichen Volume von "C: \\ Database \\ \* . mdb" und eine [**VSS- \_ Momentaufnahme- \_ Prop**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) -Instanz von snapprop erhalten, erhalten Sie den Pfad auf dem schattenkopierten Volume durch Verkettung von snappropm " \_ pwszshadow copydeviceobject", " \\ " und " \\ Database \\ \* . mdb".</span><span class="sxs-lookup"><span data-stu-id="55033-111">For example, given a path on the original volume of "C:\\DATABASE\\\*.mdb" and a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) instance of snapProp, you would obtain the path on the shadow copied volume by concatenating snapPropm\_pwszShadow copyDeviceObject, "\\", and "\\DATABASE\\\*.mdb".</span></span>

<span data-ttu-id="55033-112">Die VSS-Datei Sätze enthalten möglicherweise Platzhalter Zeichen in ihren Dateideskriptoren, sodass das Abrufen einer vollständigen Liste der Dateien in einer Schatten Kopie, die von einer Komponente verwaltet wird, möglicherweise die Verwendung von Methoden wie " **FindFileFirst**", " **findfilefirstex**" und " **FindNextFile**" erfordert.</span><span class="sxs-lookup"><span data-stu-id="55033-112">The VSS file sets might have wildcard characters in their file descriptors, so obtaining a full list of the files on a shadow copy managed by a component might require the use of methods such as **FindFileFirst**, **FindFileFirstEx**, and **FindNextFile**.</span></span>

 

 



