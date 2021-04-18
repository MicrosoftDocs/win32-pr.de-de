---
description: Die getinterfakeinfo-Funktion füllt einen Zeiger auf eine IP- \_ Schnittstellen \_ Informationsstruktur mit Informationen zu den dem System zugeordneten Schnittstellen.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Verwalten von Schnittstellen mithilfe von getinterfacetten Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8ad420f8a2d4fdbacc2bf01e65f5d9fbc9d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354460"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a>Verwalten von Schnittstellen mithilfe von getinterfacetten Info

Die [**getinterfakeinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) -Funktion füllt einen Zeiger auf eine [**IP- \_ Schnittstellen \_**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) Informationsstruktur mit Informationen zu den dem System zugeordneten Schnittstellen.

**So verwenden Sie getinterfacetten Info**

1.  Deklarieren Sie einen Zeiger auf ein [**IP- \_ Schnittstellen \_ Info**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) Objekt mit `pInfo` dem Namen und ein **ulong** -Objekt mit dem Namen `ulOutBufLen` . Deklarieren Sie auch ein **DWORD** -Objekt mit dem Namen `dwRetVal` (für die Fehlerüberprüfung verwendet).
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  Zuweisen von Arbeitsspeicher für die Strukturen.
    > [!Note]  
    > Die Größe von `ulOutBufLen` reicht nicht aus, um die Informationen zu speichern. Weitere Informationen finden Sie im nächsten Schritt.

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  Erstellen Sie zunächst [**getinterfacetten**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) Info, um die benötigte Größe in der `ulOutBufLen` Variablen abzurufen.
    > [!Note]  
    > Dieser Aufrufe der-Funktion soll fehlschlagen, und wird verwendet, um sicherzustellen, dass die `ulOutBufLen` Variable eine ausreichende Größe für alle Informationen angibt, die an zurückgegeben werden `pInfo` . Dies ist ein gängiges Programmiermodell im IP-Hilfsprogramm für Datenstrukturen und Funktionen dieses Typs.

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  Erstellen Sie einen zweiten get-Befehl für " [**getinterfacetten Info**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) " mit allgemeiner Fehlerüberprüfung, und geben Sie den Wert an die **DWORD** -Variable zurück `dwRetVal` (für eine erweiterte Fehlerüberprüfung).
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  Wenn der-Befehl erfolgreich ausgeführt wurde, greifen Sie auf die Daten aus der `pInfo` Datenstruktur zu.

    ```C++
            printf("  GetInterfaceInfo succeeded.\n");

            printf("  Num Adapters: %ld\n\n", pInterfaceInfo->NumAdapters);
            for (i = 0; i < (unsigned int) pInterfaceInfo->NumAdapters; i++) {
                printf("  Adapter Index[%d]: %ld\n", i,
                       pInterfaceInfo->Adapter[i].Index);
                printf("  Adapter Name[%d]:  %ws\n\n", i,
                       pInterfaceInfo->Adapter[i].Name);
            }
        }
    ```

    

    > [!Note]  
    > Das% WS in der ersten Zeile bezeichnet eine Breite Zeichenfolge. Dies wird verwendet, da das **namens** Attribut der [**IP- \_ Adapter \_ Index \_**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Struktur `Adapter` ein **WCHAR**-Zeichen ist, bei dem es sich um eine Unicode-Zeichenfolge handelt.

     

6.  Gibt den für die *pinfo* -Struktur zugeordneten Arbeitsspeicher frei.
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

Nächster Schritt: [Verwalten von IP-Adressen mit getipaddrtable](managing-ip-addresses-using-getipaddrtable.md)

Vorheriger Schritt: [Verwalten von Netzwerkadaptern mit getadaptersinfo](managing-network-adapters-using-getadaptersinfo.md)

 

 



