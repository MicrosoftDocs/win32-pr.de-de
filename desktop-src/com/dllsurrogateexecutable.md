---
title: Dllsurrogateausführ Bare Datei
description: Ermöglicht das Ausführen von DLL-Servern in einem benutzerdefinierten Ersatzprozess in Verbindung mit dem Registrierungs Wert dllersatz. Wenn dllsurrogateexe nicht angegeben wird, übergibt com den Wert NULL als Wert für den ersten Parameter der Funktion "deateprocess".
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- Dllsurrogateausführ barer Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106338498"
---
# <a name="dllsurrogateexecutable"></a>Dllsurrogateausführ Bare Datei

Ermöglicht das Ausführen von DLL-Servern in einem benutzerdefinierten Ersatzprozess in Verbindung mit dem Registrierungs Wert [**dllersatz**](dllsurrogate.md) . Wenn **dllsurrogateexe** nicht angegeben wird, übergibt com den Wert **null** als Wert für den ersten Parameter der Funktion " [**deateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) ".

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a>Bemerkungen

Dieser Wert ist vom Typ **reg \_ SZ**. Dies funktioniert in Verbindung mit dem [**dllersatz**](dllsurrogate.md) -Wert, um Mehrdeutigkeit bei Verwendung [**der Funktion "**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) Funktion" zu vermeiden. **Dllersatz** gibt an, ob ein benutzerdefiniertes Ersatz Zeichen verwendet werden muss. diese Informationen werden als erster Parameter für " **kreateprocess**" übergeben. Abhängig von der Implementierung von " **kreateprocess**" sind diese Informationen möglicherweise mehrdeutig. Wenn **dllsurrogateexe** angegeben wird, übergibt com den Wert als ersten Parameter von " **kreateprocess**". Wenn **dllsurrogateexe** nicht angegeben wird, übergibt com den Wert **null** als Wert für den ersten Parameter von " **kreateprocess**".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Coregisterersatz**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[DLL-Surrogates](dll-surrogates.md)
</dt> <dt>

[**Dllersatz**](dllsurrogate.md)
</dt> <dt>

[**Isurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 