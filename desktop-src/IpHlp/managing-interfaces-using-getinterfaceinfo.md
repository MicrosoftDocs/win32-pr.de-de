---
description: Die GetInterfaceInfo-Funktion füllt einen Zeiger auf eine IP INTERFACE INFO-Struktur mit Informationen zu den Schnittstellen, \_ die dem System zugeordnet \_ sind.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Verwalten von Schnittstellen mit GetInterfaceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc2afa6fe0b520e1cc5f952b44bc94052b630f4335bd739b4d7c3582d16e277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146743"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a>Verwalten von Schnittstellen mit GetInterfaceInfo

Die [**GetInterfaceInfo-Funktion**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) füllt einen Zeiger auf eine [**IP INTERFACE \_ \_ INFO-Struktur**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) mit Informationen zu den Schnittstellen, die dem System zugeordnet sind.

**So verwenden Sie GetInterfaceInfo**

1.  Deklarieren Sie einen Zeiger auf ein [**IP \_ INTERFACE \_ INFO-Objekt**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) mit dem Namen `pInfo` und ein **ULONG-Objekt** mit dem Namen `ulOutBufLen` . Deklarieren Sie auch **ein DWORD-Objekt** namens `dwRetVal` (wird für die Fehlerüberprüfung verwendet).
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  Ordnen Sie Arbeitsspeicher für die Strukturen zu.
    > [!Note]  
    > Die Größe von `ulOutBufLen` reicht nicht aus, um die Informationen zu enthalten. Weitere Informationen finden Sie im nächsten Schritt.

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  Rufen Sie zunächst [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) auf, um die für die Variable benötigte Größe `ulOutBufLen` zu erhalten.
    > [!Note]  
    > Dieser Aufruf der -Funktion ist für einen Fehler gedacht und wird verwendet, um sicherzustellen, dass die Variable eine Größe angibt, die ausreicht, um alle an zurückgegebenen `ulOutBufLen` Informationen zu `pInfo` enthalten. Dies ist ein gängiges Programmiermodell im IP-Hilfsprogramm für Datenstrukturen und Funktionen dieses Typs.

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  Führen Sie einen zweiten Aufruf von [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) mit allgemeiner Fehlerüberprüfung durch, und geben Sie den Wert an die **DWORD-Variable** zurück (für eine erweiterte `dwRetVal` Fehlerüberprüfung).
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  Wenn der Aufruf erfolgreich war, greifen Sie über die Datenstruktur `pInfo` auf die Daten zu.

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
    > %ws in der ersten Zeile gibt eine breite Zeichenfolge an. Dies wird verwendet, da das **Name-Attribut** der INDEX MAP-Struktur des [**\_ \_ \_ IP-Adapters**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) ein WCHAR ist, bei dem es `Adapter` sich um eine Unicode-Zeichenfolge handelt. 

     

6.  Geben Sie den für die *pInfo-Struktur zugeordneten Arbeitsspeicher* frei.
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

Nächster Schritt: [Verwalten von IP-Adressen mit GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

Vorheriger Schritt: [Verwalten von Netzwerkadaptern mit GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

 

 



