---
title: ActivateAtStorage
description: Konfiguriert den Client zum Instanziieren von Objekten auf demselben Computer wie der persistente Zustand, den sie verwenden oder von dem sie initialisiert werden.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8087313b8527ed95e7122d0e8dbe4fbd1ef028d7009f25937b3dc4300e9a4103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048898"
---
# <a name="activateatstorage"></a>ActivateAtStorage

Konfiguriert den Client zum Instanziieren von Objekten auf demselben Computer wie der persistente Zustand, den sie verwenden oder von dem sie initialisiert werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ SZ-Wert.** Jeder Wert, der mit "Y" oder "y" beginnt, gibt an, dass **ActivateAtStorage** verwendet werden soll.

Die **ActivateAtStorage-Funktion** bietet eine transparente Möglichkeit, clients zu ermöglichen, ausgeführte Objekte auf demselben Computer wie die von ihnen verwendeten Daten zu finden. Dies reduziert den Netzwerkdatenverkehr, da das -Objekt lokale Dateisystemaufrufe statt Aufrufe über das Netzwerk ausführt.

Wenn ein Wert für **ActivateAtStorage** festgelegt wird, wird dies das Standardverhalten bei Aufrufen der Funktionen [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) und [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) sowie der Dateimonikerimplementierung von [**IMoniker::BindToObject.**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) Bei allen diesen Aufrufen überschreibt das Angeben einer [**COSERVERINFO-Struktur**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) die Einstellung von **ActivateAtStorage** für die Dauer des Funktionsaufrufs. Der Aufrufer kann **COSERVERINFO-Informationen** über die [**BIND \_ OPTS2-Struktur**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) an **IMoniker::BindToObject** übergeben.

Der für **ActivateAtStorage** festgelegte Wert ist auch das Standardverhalten, wenn CLSCTX \_ REMOTE SERVER angegeben \_ wird, wenn keine Registrierungsinformationen für die Klasse auf dem Computer des Clients installiert sind. Clientanwendungen, die zur Nutzung von **ActivateAtStorage** geschrieben wurden, erfordern daher möglicherweise weniger Verwaltung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[Registrieren von COM-Servern](registering-com-servers.md)
</dt> </dl>

 

 