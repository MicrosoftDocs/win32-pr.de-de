---
title: Schalter "/dlldata"
description: Der Schalter /dlldata wird verwendet, um den Dateinamen für die generierte dlldata-Datei für eine Proxy-DLL anzugeben. Der Standarddateiname Dlldata.c wird verwendet, wenn der Schalter /dlldata nicht angegeben ist.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- /dlldata switch MIDL
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1274226ae9768d45bb11e1a1f5b55caeddcc247a74a7ac08e03e3fcdacb0e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105640"
---
# <a name="dlldata-switch"></a>Schalter "/dlldata"

Der Schalter **/dlldata** wird verwendet, um den Dateinamen für die generierte dlldata-Datei für eine Proxy-DLL anzugeben. Der Standarddateiname Dlldata.c wird verwendet, wenn der Schalter **/dlldata** nicht angegeben ist.

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Dateiname* 
</dt> <dd>

Der Name der C-Quelldatei, die der MIDL-Compiler für die Proxy-DLL generiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die durch den Dateinamen angegebene Datei muss mit der *Proxy-DLL* verknüpft werden. Die dlldata-Datei enthält Einstiegspunkte und Datenstrukturen, die von der Klassenfactory für die Proxy-DLL benötigt werden. Diese Datenstrukturen geben die in der Proxy-DLL enthaltenen Objektschnittstellen an. Die dlldata-Datei gibt auch den Klassenbezeichner der Klassenfactory für die Proxy-DLL an. Dies ist immer die UUID (IID) der ersten Schnittstelle der ersten Proxydatei (in alphabetischer Reihenfolge).

Die gleiche dlldata-Datei sollte beim Aufrufen von MIDL für alle IDL-Dateien angegeben werden, die in eine bestimmte Proxy-DLL gelangen. Die dlldata-Datei wird während jeder MIDL-Kompilierung erstellt oder aktualisiert, wobei inkrementell eine Liste der Schnittstellen erstellt wird, die in die Proxy-DLL aufgenommen werden.

## <a name="examples"></a>Beispiele

**midl /dlldata data.c**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




