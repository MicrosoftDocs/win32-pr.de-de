---
description: Enthält Zeiger auf Rückruffunktionen, die von CSP-Funktionen (Cryptographic Service Provider) verwendet werden können.
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: VTableProvStruc-Struktur (Cspdk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 2815d12735023cd0f7ac60fc2ed9f60fc56e32d0f54610f295a2e6b0544e589c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970866"
---
# <a name="vtableprovstruc-structure"></a>VTableProvStruc-Struktur

Die **VTableProvStruc-Struktur** enthält Zeiger auf Rückruffunktionen, die von CSP-Funktionen [*(Cryptographic Service Provider)*](../secgloss/c-gly.md) verwendet werden können.

## <a name="syntax"></a>Syntax


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a>Member

<dl> <dt>

**Version**
</dt> <dd>

Ein **DWORD-Wert,** der die Version der -Struktur angibt. Es werden drei Versionen dieser Struktur verwendet. Die Versionen sind 1, 2 und 3 und bestimmen, welche Member der Struktur gültig sind. Member der Version 1 sind auf allen Systemen gültig, die diese Struktur unterstützen.

Dies ist ein Mitglied der Version 1.

</dd> <dt>

**FuncVerifyImage**
</dt> <dd>

Die Adresse einer [**FuncVerifyImage-Rückruffunktion,**](funcverifyimage.md) die der CSP verwendet, um die Signatur aller DLLs zu überprüfen, die der CSP lädt. Alle Hilfs-DLLs, in denen ein CSP Funktionsaufrufe vornimmt, müssen auf die gleiche Weise (und mit demselben Schlüssel) wie die primäre CSP-DLL signiert werden. Um diese Signatur sicherzustellen, müssen die zusätzlichen DLLs dynamisch mithilfe der [**LoadLibrary-Funktion**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) geladen werden. Bevor die DLL geladen wird, muss jedoch die Signatur der DLL überprüft werden. Der CSP führt diese Überprüfung durch, indem er die **Funktion FuncVerifyImage** aufruft, wie im folgenden Beispiel gezeigt.

Dieser Funktionszeiger kann gespeichert und verwendet werden, bis der CSP-Kontext freigegeben wird.

Dies ist ein Mitglied der Version 1.

</dd> <dt>

**FuncReturnhWnd**
</dt> <dd>

Die Adresse einer [**FuncReturnhWnd-Rückruffunktion,**](funcreturnhwnd.md) die das Fensterhandle zurückgibt, das der CSP als übergeordnetes Element oder Besitzer einer angezeigten Benutzeroberfläche verwenden soll. CSPs, die nicht direkt mit dem Benutzer kommunizieren, und CSPs, die dedizierte Hardware für diesen Zweck verwenden, können diesen Eintrag ignorieren. Dieses Fensterhandle ist standardmäßig 0 (null), aber eine Anwendung kann dies mithilfe der [**CryptSetProvParam-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) auf einen anderen Wert festlegen, um die **PP CLIENT \_ \_ HWND-Eigenschaft** festzulegen.

Dieser Funktionszeiger kann gespeichert und verwendet werden, bis der CSP-Kontext freigegeben wird.

Dies ist ein Mitglied der Version 1.

</dd> <dt>

**dwProvType**
</dt> <dd>

Ein **DWORD-Wert,** der den Typ des anbieters angibt, der erworben werden soll. Die folgenden [*Anbietertypen*](../secgloss/p-gly.md) sind vordefiniert und werden unter [CSP-Interoperabilität](https://www.bing.com/search?q=CSP+Interoperability)ausführlich erläutert:

-   PROV \_ RSA \_ FULL
-   PROV \_ RSA \_ SIG
-   PROV \_ DSS
-   PROV \_ FORTEZZA
-   PROV \_ MS \_ EXCHANGE

Dies ist ein Mitglied der Version 2.

</dd> <dt>

**pbContextInfo**
</dt> <dd>

Ein Zeiger auf ein Array von Kontextinformationen. Die Member **pbContextInfo** und **cbContextInfo** bestimmen zusammen den Informationssatz, der verwendet wird, wenn eine [**CPSetProvParam-Funktion**](https://www.bing.com/search?q=**CPSetProvParam**) mit pp context info set aufgerufen \_ \_ wird.

Dies ist ein Mitglied der Version 2.

</dd> <dt>

**cbContextInfo**
</dt> <dd>

Ein **DWORD-Wert,** der die Anzahl der Elemente im **pbContextInfo-Array** angibt.

Dies ist ein Mitglied der Version 2.

</dd> <dt>

**pszProvName**
</dt> <dd>

Eine Zeichenfolge, die den Namen des Anbieters enthält.

Dies ist ein Mitglied der Version 3.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Zeiger in der **VTableProvStruc-Struktur** sind nur innerhalb der [**CPAcquireContext-Funktion**](https://www.bing.com/search?q=**CPAcquireContext**) verfügbar. Wenn Member der -Struktur benötigt werden, nachdem ein Aufruf von **CPAcquireContext** abgeschlossen wurde, müssen Kopien der erforderlichen Strukturelemente vom CSP erstellt werden. Die Funktionszeiger in dieser Struktur können gespeichert und verwendet werden, bis der CSP-Kontext freigegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cspdk.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **VTableProvStrucW** (Unicode)<br/>                                          |



 

 
