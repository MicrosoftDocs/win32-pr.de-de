---
description: Protokollieren von topologieknotenaktivitäten
ms.assetid: 853b3900-1214-43b9-bf0e-e45c1159c5f1
title: Protokollieren von topologieknotenaktivitäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ca83d0513b97d053e27388bd0f2a418dfb253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041876"
---
# <a name="logging-topology-node-activities"></a>Protokollieren von topologieknotenaktivitäten

Topoedit bietet die Option zum Erfassen von Protokollierungs Informationen für einen Transformations Knoten oder einen Ausgabe Knoten einer Topologie.

## <a name="to-setup-logging"></a>Einrichten der Protokollierung

1.  Wählen Sie im Bereich **Topologie** einen Transformations Knoten oder einen Ausgabe Knoten aus, indem Sie darauf klicken.

2.  Klicken Sie **im Menü** Extras auf **ausgewählten Knoten Spy**.

Während der topologiebildung werden alle Methodenaufrufe für den ausgewählten Knoten in einer Textdatei protokolliert. Diese wird in dem Ordner gespeichert, in dem sich die Mediendatei befindet. Die Protokolldatei wird mit dem Knoten Namen und dem eindeutigen Knoten Bezeichner für die Topologie gespeichert. Dadurch wird sichergestellt, dass kein anderer Knoten in das Protokoll schreibt. Um den Bezeichner Programm gesteuert abzurufen, nennen Sie [**imftopologynode:: gettoponodeid**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).

Im folgenden finden Sie einen Auszug aus einer Protokolldatei.

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729720 1 02729760) returns 80004001`

`GetInputCurrentType(0 02C9F4A4) returns c00d6d60`

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729760 1 02729720) returns 80004001`

`SetInputType(0 0012F8D8 0) returns 0`

`--> Arg(2, in) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=WMAudioV8, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=2048, AVG_BYTES_PER_SECOND=12000, BITS_PER_SAMPLE=16, USER_DATA=<BLOB>, {9D62927D-36BE-4CF2-B5C4-A3926E3E8711}=5760, {9D62927F-36BE-4CF2-B5C4-A3926E3E8711}=674,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputCurrentType(0 02C9F4B0) returns c00d6d60`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729640 1 02729720) returns 80004001`

`GetOutputAvailableType(0 0 02C9F4B0) returns 0`

`--> Arg(3, out) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=Float, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=8, AVG_BYTES_PER_SECOND=384000, BITS_PER_SAMPLE=32, ALL_SAMPLES_INDEPENDENT=1, FIXED_SIZE_SAMPLES=1,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputAvailableType(0 1 02C9F4B0) returns 0`

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Topoedit](topoedit.md)
</dt> </dl>

 

 



