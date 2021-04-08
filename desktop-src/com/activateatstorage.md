---
title: Activateatstorage
description: Konfiguriert den Client für die instanzialisierung von Objekten auf dem gleichen Computer wie der persistente Zustand, den Sie verwenden oder von dem Sie initialisiert werden.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2ddd1330191d7b7baf37973dbfb40e267a2f87e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039696"
---
# <a name="activateatstorage"></a>Activateatstorage

Konfiguriert den Client für die instanzialisierung von Objekten auf dem gleichen Computer wie der persistente Zustand, den Sie verwenden oder von dem Sie initialisiert werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert. Jeder Wert, der mit "y" oder "y" beginnt, gibt an, dass **activateatstorage** verwendet werden soll.

Die **activateatstorage** -Funktion bietet eine transparente Möglichkeit, um Clients das Auffinden von laufenden Objekten auf dem gleichen Computer wie die Daten zu ermöglichen, die Sie verwenden. Dadurch wird der Netzwerkverkehr reduziert, da das Objekt anstelle von Aufrufen über das Netzwerk lokale Dateisystem Aufrufe ausführt.

Wenn ein Wert für **activateatstorage** festgelegt wird, wird dies zum Standardverhalten bei Aufrufen der Funktionen [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) und [**cogetinstancefromistorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) sowie für die Datei-monikerimplementierung von [**IMoniker:: BindTo Object**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). Bei allen diesen Aufrufen überschreibt die Angabe einer [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur die Einstellung von **activateatstorage** für die Dauer des Funktionsaufrufs. Der Aufrufer kann **COSERVERINFO** -Informationen über die [**Bind \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) -Struktur an **IMoniker:: BindToObject** übergeben.

Der für **activateatstorage** festgelegte Wert ist auch das Standardverhalten, wenn der CLSCTX- \_ Remote \_ Server angegeben wird, wenn auf dem Client Computer keine Registrierungsinformationen für die Klasse installiert sind. Client Anwendungen, die für die Nutzung von **activateatstorage** geschrieben wurden, benötigen daher möglicherweise weniger Verwaltung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[**Cogetinstancefromistorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[**IMoniker:: bindtoken Object**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> </dl>

 

 