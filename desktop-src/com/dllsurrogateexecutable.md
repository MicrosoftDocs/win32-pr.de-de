---
title: DllSurrogateExecutable
description: Ermöglicht die Ausführung von DLL-Servern in einem benutzerdefinierten Ersatzprozess in Verbindung mit dem DllSurrogate-Registrierungswert. Wenn DllSurrogateExecutable nicht angegeben ist, übergibt COM NULL als Wert für den ersten Parameter der CreateProcess-Funktion.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- DllSurrogateExecutable-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fc12af22d1f85c2d2e5ff6e75b2904c5fc5eea636a64e314f997ff36a44e38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373380"
---
# <a name="dllsurrogateexecutable"></a>DllSurrogateExecutable

Ermöglicht die Ausführung von DLL-Servern in einem benutzerdefinierten Ersatzprozess in Verbindung mit dem [**DllSurrogate-Registrierungswert.**](dllsurrogate.md) Wenn **DllSurrogateExecutable** nicht angegeben ist, übergibt COM **NULL** als Wert für den ersten Parameter der [**CreateProcess-Funktion.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a>Hinweise

Dieser Wert ist vom Typ **REG \_ SZ.** Er arbeitet mit dem [**DllSurrogate-Wert**](dllsurrogate.md) zusammen, um Mehrdeutigkeiten bei der Verwendung der [**CreateProcess-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) zu vermeiden. **DllSurrogate** gibt an, ob ein benutzerdefiniertes Ersatzzeichen verwendet werden muss, und diese Informationen werden als erster Parameter für **CreateProcess** übergeben. Abhängig von der Implementierung von **CreateProcess** können diese Informationen mehrdeutig sein. Wenn **DllSurrogateExecutable** angegeben ist, übergibt COM den Wert als ersten Parameter von **CreateProcess.** Wenn **DllSurrogateExecutable** nicht angegeben ist, übergibt COM **NULL** als Wert für den ersten Parameter von **CreateProcess.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[DLL-Ersatzzeichen](dll-surrogates.md)
</dt> <dt>

[**DllSurrogate**](dllsurrogate.md)
</dt> <dt>

[**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 