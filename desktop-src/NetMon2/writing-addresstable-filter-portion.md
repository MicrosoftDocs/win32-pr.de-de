---
description: Der Adress Filter benachrichtigt den Netzwerkmonitor Treiber, Frames zu akzeptieren, die über eine Vielzahl von angegebenen Mac-Adresstypen verfügen (Ethernet, TokenRing und FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Schreiben des "adresssstable"-Filter Teils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362930"
---
# <a name="writing-addresstable-filter-portion"></a>Schreiben des "adresssstable"-Filter Teils

Der Adress Filter benachrichtigt den Netzwerkmonitor Treiber, Frames zu akzeptieren, die über eine Vielzahl von angegebenen Mac-Adresstypen verfügen (Ethernet, TokenRing und FDDI). Sie können maximal acht Adress Paare angeben. Ein Adress Paar kann eine Quelle, ein Ziel, beides oder keines von beiden angeben.

Der Adress Teil des Filters besteht aus zwei Strukturen: [**adresssstable**](addresstable.md) und [**adresssspair**](addresspair.md).

Wenn Sie keine Adressen angeben, werden alle Rahmen an den Adress Filter übergeben. Wenn Sie jedoch Adressen angeben, werden nur die Rahmen übergeben, die den angegebenen Adress Filter übergeben.

Das Entwickeln des Adress Filters umfasst das Zuordnen einer [**adressstabilen**](addresstable.md) Struktur und das Ausfüllen von Membern der [**adresspair**](addresspair.md) -Struktur.

**So erstellen Sie den Adress Teil eines Erfassungs Filters**

1.  Verwenden Sie das Flag **capturefilter \_ Flags \_ local \_ only** der [**capturefilter**](capturefilter.md) -Struktur, um die Erfassung auf den Datenverkehr zu und von Ihrem lokalen Computer zu beschränken.

    Wenn Sie dieses Flag festlegen, wird die NIC nicht auf den gemischten-Modus festgelegt. die Erfassungs Datei erfasst nur den lokalen Datenverkehr.

2.  Verwenden Sie den folgenden Beispielcode zum Definieren der " [**adresssstable**](addresstable.md) "-Struktur:

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  Verwenden Sie die in der folgenden Tabelle aufgeführten Informationen, um einen [**adresspair**](addresspair.md) -flagtyp auszuwählen. 

    | Flag                             | Bedeutung                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | \_adressflags \_ entsprechen " \_ DST"       | Entspricht einer Zieladresse.                                                        |
    | \_adressflags \_ entsprechen \_ src       | Entspricht einer Quelladresse                                                              |
    | \_Ausschließen von adressflags \_          | Schließt den Frame aus, wenn diese Adresse gefunden wird (entweder eine definierte Quelle oder ein Ziel). |
    | \_adressflags \_ DST \_ Group \_ addr | Entspricht dem Gruppen Bit (der Zieladresse) nur für Broadcast-/typnachrichten.      |
    | \_adressflags \_ stimmen mit \_ beiden identisch.      | Entspricht der Ziel-und der Quelladresse.                                    |

    

     

4.  Geben Sie eine Zieladresse ein, die mit dem von Ihnen ausgewählten [**adresssspair**](addresspair.md) -Flag ausgewertet wird.
5.  Geben Sie eine Quelladresse ein, die mit dem von Ihnen ausgewählten [**adresssspair**](addresspair.md) -Flag ausgewertet wird.
6.  Füllen Sie die " [**adresstable**](addresstable.md) "-Struktur mit einem Array von [**adresssspair**](addresspair.md) -Strukturen, das die vom Treiber auswerteten Adress Paare enthält. Alle Adress Paare werden als logische OR-Anweisung ausgewertet (adresspair 1 \| \| adresssspair 2). Sie können maximal acht Adress Paare in einen Erfassungs Filter einschließen.

 

 



