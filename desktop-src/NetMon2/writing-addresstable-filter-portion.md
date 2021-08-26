---
description: Der Adressfilter benachrichtigt den Netzwerkmonitor Treiber, Frames mit einer Vielzahl von angegebenen MAC-Adresstypen (Ethernet, Token Ring und FDDI) zu akzeptieren.
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Schreiben des ADDRESSTABLE-Filterteils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a18f8004ea4c38607d6c1c7b8fa741315b41fefe5b4d31b103167d415eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128790"
---
# <a name="writing-addresstable-filter-portion"></a>Schreiben des ADDRESSTABLE-Filterteils

Der Adressfilter benachrichtigt den Netzwerkmonitor Treiber, Frames mit einer Vielzahl von angegebenen MAC-Adresstypen (Ethernet, Token Ring und FDDI) zu akzeptieren. Sie können maximal acht Adresspaare angeben. Ein Adresspaar kann eine Quelle, ein Ziel, beide oder keines angeben.

Der Adressteil des Filters besteht aus zwei Strukturen: [**ADDRESSTABLE**](addresstable.md) und [**ADDRESSPAIR.**](addresspair.md)

Wenn Sie KEINE Adressen angeben, übergeben ALLE Frames den Adressfilter. Wenn Sie jedoch Adressen angeben, werden nur die Frames übergeben, die den angegebenen Adressfilter übergeben.

Das Erstellen des Adressfilters umfasst das Zuordnen einer [**ADDRESSTABLE-Struktur**](addresstable.md) und das Ausfüllen von Membern der [**ADDRESSPAIR-Struktur.**](addresspair.md)

**So erstellen Sie den Adressteil eines Erfassungsfilters**

1.  Verwenden Sie das **CAPTUREFILTER \_ FLAGS \_ LOCAL \_ ONLY-Flag** der [**CAPTUREFILTER-Struktur,**](capturefilter.md) um die Erfassung auf Datenverkehr zu und von Ihrem lokalen Computer zu beschränken.

    Wenn Sie dieses Flag festlegen, wird die NIC nicht auf den promiscuous-Modus festgelegt. Die Erfassungsdatei erfasst nur lokalen Datenverkehr.

2.  Verwenden Sie den folgenden Beispielcode, um die [**ADDRESSTABLE-Struktur**](addresstable.md) zu definieren:

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

3.  Verwenden Sie die in der folgenden Tabelle aufgeführten Informationen, um einen [**ADDRESSPAIR-Flagtyp**](addresspair.md) auszuwählen. 

    | Flag                             | Bedeutung                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | \_ADRESSFLAGS \_ STIMMEN MIT \_ DST ÜBEREIN       | Entspricht einer Zieladresse.                                                        |
    | ADDRESS \_ FLAGS \_ MATCH \_ SRC       | Entspricht einer Quelladresse                                                              |
    | \_AUSSCHLIEßEN VON ADRESSFLAGS \_          | Schließt den Frame aus, wenn diese Adresse gefunden wird (entweder eine definierte Quelle oder ein Ziel). |
    | \_ADRESSFLAGS \_ DST GROUP \_ \_ ADDR | Entspricht Gruppenbits (der Zieladresse) nur für Nachrichten vom Typ Broadcast.      |
    | \_ADRESSFLAGS STIMMEN MIT \_ BEIDEN ÜBEREIN. \_      | Entspricht sowohl der Ziel- als auch der Quelladresse.                                    |

    

     

4.  Geben Sie eine Zieladresse ein, die anhand des von Ihnen ausgewählten [**ADDRESSPAIR-Flags**](addresspair.md) ausgewertet wird.
5.  Geben Sie eine Quelladresse ein, die anhand des von Ihnen ausgewählten [**ADDRESSPAIR-Flags**](addresspair.md) ausgewertet wird.
6.  Füllen Sie die [**ADDRESSTABLE-Struktur**](addresstable.md) mit einem Array von [**ADDRESSPAIR-Strukturen**](addresspair.md) auf, das die Adresspaare enthält, die der Treiber auswertet. Alle Adresspaare werden als logische OR-Anweisung ausgewertet (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2). Sie können maximal acht Adresspaare in einen Erfassungsfilter einschließen.

 

 



