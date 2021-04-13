---
title: Dllersatz
description: Ermöglicht das Ausführen von DLL-Servern in einem Ersatz Vorgang. Wenn eine leere Zeichenfolge angegeben wird, wird das vom System bereitgestellte Ersatz Zeichen verwendet. Andernfalls gibt der Wert den Pfad des zu verwendenden Ersatz Zeichens an.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- Dllersatz-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391062"
---
# <a name="dllsurrogate"></a>Dllersatz

Ermöglicht das Ausführen von DLL-Servern in einem Ersatz Vorgang. Wenn eine leere Zeichenfolge angegeben wird, wird das vom System bereitgestellte Ersatz Zeichen verwendet. Andernfalls gibt der Wert den Pfad des zu verwendenden Ersatz Zeichens an.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert, der angibt, dass es sich bei der Klasse um eine DLL handelt, die in einem Ersatzprozess aktiviert werden soll, und um den zu verwendenden Ersatzprozess zu verwenden. Legen Sie den *Pfad* auf eine leere Zeichenfolge oder auf **null** fest, um den vom System bereitgestellten generischen Ersatzprozess zu verwenden. Wenn Sie einen anderen Ersatzprozess angeben möchten, legen Sie den *Pfad* auf den Pfad des Ersatz Zeichens fest. Wie in der Angabe des Pfads eines Servers unter dem Schlüssel [**LocalServer32**](localserver32.md) ist eine vollständige Pfadspezifikation nicht erforderlich. Das Ersatz Zeichen muss geschrieben werden, um ordnungsgemäß mit dem DCOM-Dienst zu kommunizieren, wie in [Schreiben eines benutzerdefinierten Ersatz](writing-a-custom-surrogate.md)Zeichens beschrieben.

Der **dllersatz** -Wert muss vorhanden sein, damit ein dll-Server in einem Ersatz Zeichen aktiviert werden muss. Die Aktivierung bezieht sich auf einen Aufrufen von " [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)", " [**cokreateinstanceex**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)", " **cokreateinstanceex**", " [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)", " [**cogetinstancefromistorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)" oder " [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)". Das Ausführen von DLLs in einem Ersatzprozess bietet die Vorteile einer ausführbaren Implementierung, einschließlich der Fehler Isolation, der Möglichkeit, mehrere Clients gleichzeitig zu bedienen, und ermöglicht es dem Server, Dienste für Remote Clients in einer verteilten Umgebung bereitzustellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Coregisterersatz**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[DLL-Surrogates](dll-surrogates.md)
</dt> <dt>

[**Dllsurrogateausführ Bare Datei**](dllsurrogateexecutable.md)
</dt> <dt>

[**Isurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 