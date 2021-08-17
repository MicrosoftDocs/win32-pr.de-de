---
description: Wird zur Darstellung von Registrierungseinträgen verwendet, die die Zwischenspeicherung privater Schlüssel durch softwarebasierte CSPs von Microsoft steuern.
ms.assetid: 67909072-72fe-4777-ae52-a7b9047c9dd5
title: Zwischenspeicherungskonstten für private Schlüssel (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d4caf6a3973a5113e03cbe24882241609ff83b8be65a20492f8f967abb734f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978561"
---
# <a name="private-key-caching-constants"></a>Zwischenspeicherungskonstten für private Schlüssel

Die folgenden Konstanten werden verwendet, um Registrierungseinträge zu darstellen, die die Zwischenspeicherung privater Schlüssel [*durch*](../secgloss/p-gly.md) softwarebasierte CSPs von Microsoft steuern.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                                                                                    | Beschreibung                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| <span id="szKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><span id="szkey_cryptoapi_private_key_options"></span><span id="SZKEY_CRYPTOAPI_PRIVATE_KEY_OPTIONS"></span><dl> <dt>**szKEY \_ CRYPTOAPI \_ PRIVATE \_ KEY \_ OPTIONS**</dt> <dt>"Software Policies Microsoft \\ \\ \\ \\ \\ \\ Cryptography"</dt> </dl> | Der Pfad der Registrierungseinträge für das Zwischenspeichern des privaten Schlüssels unter dem **Stamm HKEY \_ LOCAL \_ MACHINE.**<br/> |



Die folgenden Konstanten werden verwendet, um Registrierungswerte zu identifizieren, die die Zwischenspeicherung privater Schlüssel global für einen bestimmten Prozess durch softwarebasierte CSPs von Microsoft steuern.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="szPRIV_KEY_CACHE_MAX_ITEMS"></span><span id="szpriv_key_cache_max_items"></span><span id="SZPRIV_KEY_CACHE_MAX_ITEMS"></span><dl> <dt>**szPRIV \_ KEY \_ CACHE \_ MAX \_ ITEMS**</dt> <dt>"PrivKeyCacheMaxItems"</dt> </dl>                                                                  | Ein **REG \_ DWORD-Wert** unter dem **Registrierungsschlüssel szKEY \_ CRYPTOAPI PRIVATE KEY \_ \_ \_ OPTIONS,** der die maximale Anzahl privater Schlüssel angibt, die gleichzeitig für einen einzelnen Prozess zwischengespeichert werden können. Diese Überprüfung wird immer dann durchgeführt, wenn ein gespeicherter privater Schlüssel gelesen wird. Wenn die maximale Anzahl überschritten wird, wird der am wenigsten verwendete Schlüssel aus dem Cache entfernt.<br/> Wenn dieser Wert 0 (null) ist, werden keine Schlüssel zwischengespeichert. Wenn dieser Wert nicht vorhanden ist, wird der **Standardwert cPRIV \_ KEY CACHE MAX ITEMS \_ \_ \_ \_ DEFAULT** verwendet.<br/> Wenn auf einen privaten Schlüssel, der aus dem Cache gelöscht wird, derzeit in einem offenen Kontext verwiesen wird, wird der Schlüssel beim nächsten Versuch, den Schlüssel zu verwenden, aus dem Speicher gelesen.<br/> **Windows Server 2003 und Windows XP mit SP1 und früher:** Dieser Registrierungswert wird nicht unterstützt.<br/>                                  |
| <span id="cPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><span id="cpriv_key_cache_max_items_default"></span><span id="CPRIV_KEY_CACHE_MAX_ITEMS_DEFAULT"></span><dl> <dt>**cPRIV \_ KEY \_ CACHE MAX ITEMS \_ \_ \_ DEFAULT**</dt> <dt>20</dt> </dl>                                                         | Der Standardwert des **Registrierungseintrags szPRIV \_ KEY CACHE MAX \_ \_ \_ ITEMS,** wenn kein Wert angegeben ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="szPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><span id="szpriv_key_cache_purge_interval_seconds"></span><span id="SZPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS"></span><dl> <dt>**szPRIV \_ KEY \_ CACHE \_ PURGE INTERVAL \_ \_ SECONDS**</dt> <dt>"PrivKeyCachePurgeIntervalSeconds"</dt> </dl> | Ein **REG \_ DWORD-Wert** unter dem **Registrierungsschlüssel szKEY \_ CRYPTOAPI PRIVATE KEY \_ \_ \_ OPTIONS,** der das maximale Alter eines zwischengespeicherten privaten Schlüssels in Sekunden angibt. Diese Überprüfung wird immer dann durchgeführt, wenn ein gespeicherter privater Schlüssel verwendet oder gelesen wird. Wenn diese Zeitspanne seit dem letzten Löschen verstrichen ist, werden alle zwischengespeicherten Schlüssel, auf die seit dem letzten Löschen nicht verwiesen wurde, aus dem Cache entfernt.<br/> Wenn dieser Wert nicht vorhanden ist, wird der **Standardwert cPRIV \_ KEY CACHE \_ \_ PURGE INTERVAL SECONDS \_ \_ \_ DEFAULT** verwendet.<br/> Wenn auf einen privaten Schlüssel, der aus dem Cache entfernt wird, derzeit in einem offenen Kontext verwiesen wird, wird der Schlüssel beim nächsten Versuch, den Schlüssel zu verwenden, aus dem Speicher gelesen.<br/> **Windows Server 2003 und Windows XP mit SP1 und früher:** Dieser Registrierungswert wird nicht unterstützt.<br/> |
| <span id="cPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><span id="cpriv_key_cache_purge_interval_seconds_default"></span><span id="CPRIV_KEY_CACHE_PURGE_INTERVAL_SECONDS_DEFAULT"></span><dl> <dt>**cPRIV \_ KEY \_ CACHE \_ PURGE INTERVAL SECONDS \_ \_ \_ DEFAULT**</dt> <dt>86400</dt> </dl> | Der Standardwert des **Registrierungseintrags szPRIV \_ KEY CACHE \_ \_ PURGE INTERVAL \_ \_ SECONDS,** wenn kein Wert angegeben ist. Dieser Wert entspricht einem Tag.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



Die folgenden Konstanten werden verwendet, um Registrierungswerte zu identifizieren, die die Zwischenspeicherung privater Schlüssel für eine einzelne Microsoft-CSP-Instanz (Software-Based [*Cryptographic Service Provider)*](../secgloss/c-gly.md) steuern.



| Konstante/Wert                                                                                                                                                                                                                                                                                          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>"AllowCachePW"</dt> </dl>                                                                                                                                                         | Ein **REG \_ DWORD-Wert** unter den **HKEY LOCAL MACHINE SOFTWARE \_ Policies Microsoft \_ \\ \\ \\ \\ Cryptography Protect-Registrierungsschlüssel, \\** der angibt, ob die Kennwortzwischenspeicherung für kennwortgeschützte Schlüssel in den softwarebasierten CSPs von Microsoft aktiviert ist. Wenn dieser Wert 0 ist, wird die Zwischenspeicherung von Kennwörtern eingestellt, und der Benutzer wird bei jeder Verwendung eines kennwortgeschützten Schlüssels zur Eingabe des Kennworts aufgefordert. Jeder andere Wert oder das Fehlen dieses Werts gibt an, dass das Kennwort zwischengespeichert wird. In diesem Szenario wird der Benutzer pro Prozess nur einmal zur Eingabe eines solchen Schlüssels aufgefordert. <br/> |
| <span id="szKEY_CACHE_ENABLED"></span><span id="szkey_cache_enabled"></span><span id="SZKEY_CACHE_ENABLED"></span><dl> <dt>**szKEY \_ CACHE \_ ENABLED**</dt> <dt>"CachePrivateKeys"</dt> </dl>          | Ein **REG \_ DWORD-Wert** unter dem **Registrierungsschlüssel \_ szKEY CRYPTOAPI \_ PRIVATE KEY \_ \_ OPTIONS,** der angibt, ob die Zwischenspeicherung privater Schlüssel aktiviert ist. Wenn dieser Wert 1 ist, wird die Zwischenspeicherung privater Schlüssel aktiviert. Jeder andere Wert oder das Fehlen dieses Werts gibt an, dass die Zwischenspeicherung privater Schlüssel deaktiviert ist.<br/> **Windows Vista mit SP1, Windows Vista und Windows XP:** Dieser Registrierungswert wird nicht unterstützt.<br/>                                                                                                                                                        |
| <span id="szKEY_CACHE_SECONDS"></span><span id="szkey_cache_seconds"></span><span id="SZKEY_CACHE_SECONDS"></span><dl> <dt>**szKEY \_ CACHE \_ SECONDS**</dt> <dt>"PrivateKeyLifetimeSeconds"</dt> </dl> | Ein **REG \_ DWORD-Wert** unter dem **Registrierungsschlüssel szKEY \_ CRYPTOAPI PRIVATE KEY \_ \_ \_ OPTIONS,** der das maximale Alter eines zwischengespeicherten privaten Schlüssels in Sekunden angibt.<br/> **Windows XP:** Dieser Registrierungswert wird nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Hinweise

Die Unterschiede zwischen **den Werten szKEY \_ CACHE \_ SECONDS** und **szPRIV \_ KEY CACHE \_ \_ PURGE INTERVAL \_ \_ SECONDS** lauten wie folgt:

 **szKEY \_ CACHE \_ SECONDS**  

-   Dieser Wert gilt nur für einen bestimmten CSP. Nachdem der CSP freigegeben wurde, wird auch der Cache des CSP freigegeben.  
-   Dieser Wert wird nur angewendet, wenn versucht wird, einen bestimmten privaten Schlüssel mit einem bestimmten Kontexthand handle zu verwenden.  

**szPRIV \_ KEY \_ CACHE \_ PURGE INTERVAL \_ \_ SECONDS**  

-   Dieser Wert gilt für alle CSPs in einem Prozess. Auch wenn der CSP freigegeben wird, wird dieser Cache nicht freigegeben.  
-   Dieser Wert gilt immer dann, wenn ein gespeicherter privater Schlüssel in einem einzigen Prozess verwendet oder aus dem Speicher gelesen wird.  



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
