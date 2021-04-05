---
title: /dlldata-Schalter
description: Der Schalter/dlldata wird verwendet, um den Dateinamen für die generierte "dlldata-Datei für eine Proxy-dll anzugeben. Der Standard Dateiname "dlldata. c" wird verwendet, wenn der Schalter "/dlldata" nicht angegeben wird.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- /dlldata-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718690"
---
# <a name="dlldata-switch"></a>/dlldata-Schalter

Der Schalter **/dlldata** wird verwendet, um den Dateinamen für die generierte "dlldata-Datei für eine Proxy-dll anzugeben. Der Standard Dateiname "dlldata. c" wird verwendet, wenn der Schalter " **/dlldata** " nicht angegeben wird.

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Dateiname* 
</dt> <dd>

Der Name der C-Quelldatei, die der mittlerer l-Compiler für die Proxy-dll generiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die durch *Dateiname* angegebene Datei muss mit der Proxy-DLL verknüpft werden. Die "dlldata-Datei enthält Einstiegspunkte und Datenstrukturen, die von der Klassenfactory für die Proxy-dll benötigt werden. Diese Datenstrukturen geben die Objekt Schnittstellen an, die in der Proxy-dll enthalten sind. In der "dlldata-Datei wird auch der Klassen Bezeichner der Klassenfactory für die Proxy-dll angegeben. Dabei handelt es sich immer um die UUID (IID) der ersten Schnittstelle der ersten Proxy Datei (in alphabetischer Reihenfolge).

Die gleiche "dlldata-Datei sollte beim Aufrufen von" Mittel l "für alle IDL-Dateien angegeben werden, die in eine bestimmte Proxy-dll geleitet werden. Die "dlldata-Datei wird bei jeder mittleren Kompilierung erstellt oder aktualisiert, und es wird inkrementell eine Liste der Schnittstellen erstellt, die in die Proxy-dll aufgenommen werden.

## <a name="examples"></a>Beispiele

**Mittel l/dlldata Data. c**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




