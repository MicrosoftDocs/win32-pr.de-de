---
description: Enthält Zeiger auf Rückruf Funktionen, die von den Funktionen des Kryptografiedienstanbieters (CSP) verwendet werden können.
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: Vtableprovstruc-Struktur (cspdk. h)
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
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759457"
---
# <a name="vtableprovstruc-structure"></a>Vtableprovstruc-Struktur

Die **vtableprovstruc** -Struktur enthält Zeiger auf Rückruf Funktionen, die von den Funktionen des [*Kryptografiedienstanbieters*](../secgloss/c-gly.md) (CSP) verwendet werden können.

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

Ein **DWORD** -Wert, der die Version der-Struktur angibt. Drei Versionen dieser Struktur werden verwendet. Die Versionen sind 1, 2 und 3 und legen fest, welche Member der Struktur gültig sind. Member der Version 1 sind auf allen Systemen gültig, die diese Struktur unterstützen.

Dabei handelt es sich um ein Mitglied der Version 1.

</dd> <dt>

**Funcverifyimage**
</dt> <dd>

Die Adresse einer [**funkverifyimage**](funcverifyimage.md) -Rückruffunktion, die der CSP verwendet, um die Signatur aller DLLs zu überprüfen, die vom CSP geladen werden. Alle Erweiterungs-DLLs, in die ein CSP Funktionsaufrufe durchführt, müssen auf die gleiche Weise (und mit demselben Schlüssel) wie die primäre CSP-DLL signiert werden. Um diese Signatur sicherzustellen, müssen die zusätzlichen DLLs dynamisch mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion geladen werden. Aber bevor die dll geladen wird, muss die Signatur der dll überprüft werden. Der CSP führt diese Überprüfung durch Aufrufen der Funktion **funcverifyimage** aus, wie im folgenden Beispiel gezeigt.

Dieser Funktionszeiger kann gespeichert und verwendet werden, bis der CSP-kontextfrei gegeben wird.

Dabei handelt es sich um ein Mitglied der Version 1.

</dd> <dt>

**Funkreturnhwnd**
</dt> <dd>

Die Adresse einer [**funkreturnhwnd**](funcreturnhwnd.md) -Rückruffunktion, die das Fenster Handle zurückgibt, das der CSP als übergeordnetes Element oder Besitzer einer beliebigen angezeigten Benutzeroberfläche verwenden soll. CSPs, die nicht direkt mit dem Benutzer und CSPs kommunizieren, die für diesen Zweck dedizierte Hardware verwenden, können diesen Eintrag ignorieren. Dieses Fenster Handle ist standardmäßig auf 0 festgelegt, aber eine Anwendung kann diese auf einen anderen Wert festlegen, indem die Funktion " [**cryptsetprovparam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) " zum Festlegen der Eigenschaft " **PP-Client- \_ \_ HWND** " verwendet wird.

Dieser Funktionszeiger kann gespeichert und verwendet werden, bis der CSP-kontextfrei gegeben wird.

Dabei handelt es sich um ein Mitglied der Version 1.

</dd> <dt>

**dwprovtype**
</dt> <dd>

Ein **DWORD** -Wert, der den Typ des abzurufenden Anbieters angibt. Die folgenden [*Anbieter Typen*](../secgloss/p-gly.md) sind vordefiniert und werden in der [CSP-Interoperabilität](https://www.bing.com/search?q=CSP+Interoperability)ausführlich erläutert:

-   Prov \_ RSA \_ Full
-   Prov \_ RSA \_ sig
-   Prov- \_ DSS
-   Prov- \_ Fortezza
-   Prov \_ MS \_ Exchange

Dabei handelt es sich um ein Mitglied der Version 2.

</dd> <dt>

**pbcontextinfo**
</dt> <dd>

Ein Zeiger auf ein Array von Kontextinformationen. Die Member " **pbcontextinfo** " und " **cbcontextinfo** " bestimmen zusammen den verwendeten Informations Satz, wenn eine [**cpsetprovparam**](https://www.bing.com/search?q=**CPSetProvParam**) -Funktion mit \_ \_ festgelegtem PP-Kontext Info Satz aufgerufen wird.

Dabei handelt es sich um ein Mitglied der Version 2.

</dd> <dt>

**cbcontextinfo**
</dt> <dd>

Ein **DWORD** -Wert, der die Anzahl der Elemente im **pbcontextinfo** -Array angibt.

Dabei handelt es sich um ein Mitglied der Version 2.

</dd> <dt>

**pszprovname**
</dt> <dd>

Eine Zeichenfolge, die den Namen des Anbieters enthält.

Dabei handelt es sich um ein Mitglied der Version 3.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Zeiger in der **vtableprovstruc** -Struktur sind nur innerhalb der [**cpacquirecontext**](https://www.bing.com/search?q=**CPAcquireContext**) -Funktion verfügbar. Wenn Elemente der Struktur nach Abschluss eines Aufrufes von **cpacquirecontext** benötigt werden, müssen vom CSP Kopien der benötigten Strukturelemente erstellt werden. Die Funktionszeiger in dieser Struktur können gespeichert und verwendet werden, bis der CSP-kontextfrei gegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Vtableprovstrucw** (Unicode)<br/>                                          |



 

 
