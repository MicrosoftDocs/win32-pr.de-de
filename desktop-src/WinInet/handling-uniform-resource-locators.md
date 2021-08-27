---
title: Behandeln von einheitlichen Ressourcenlocators
description: Ein Uniform Resource Locator (URL) ist eine kompakte Darstellung des Speicherorts und der Zugriffsmethode für eine Ressource im Internet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419433c8a06b6243bf048896664a67da31a3c58d1d79eb6fea65f9fc99dbe63a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121870"
---
# <a name="handling-uniform-resource-locators"></a>Behandeln von einheitlichen Ressourcenlocators

Ein Uniform Resource Locator (URL) ist eine kompakte Darstellung des Speicherorts und der Zugriffsmethode für eine Ressource im Internet. Jede URL besteht aus einem Schema (HTTP, HTTPS oder FTP) und einer schemaspezifischen Zeichenfolge. Diese Zeichenfolge kann auch eine Kombination aus einem Verzeichnispfad, einer Suchzeichenfolge oder einem Namen der Ressource enthalten. Die WinINet-Funktionen bieten die Möglichkeit, URLs zu erstellen, zu kombinieren, aufzubrechen und zu kanonisieren. Weitere Informationen zu URLs finden Sie unter [RFC-1738](https://www.ietf.org/rfc/rfc1738.txt) unter Uniform Resource Locators (URL).

Die URL-Funktionen werden aufgabenorientiert ausgeführt. Der Inhalt und das Format der URL, die der Funktion übergeben wird, werden nicht überprüft. Die aufrufende Anwendung sollte die Verwendung dieser Funktionen nachverfolgen, um sicherzustellen, dass die Daten das beabsichtigte Format aufweisen. Beispielsweise würde die [**InternetCanonicalizeUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) das Zeichen "%" in die Escapesequenz "%25" konvertieren, wenn keine Flags verwendet werden. Wenn [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) für die kanonische URL verwendet wird, wird die Escapesequenz "%25" in die Escapesequenz "%2525" konvertiert, was nicht ordnungsgemäß funktioniert.

-   [Was ist eine kanonisierte URL?](#what-is-a-canonicalized-url)
-   [Verwenden der WinINet-Funktionen zum Verarbeiten von URLs](#using-the-wininet-functions-to-handle-urls)
-   [Kanonisieren von URLs](#what-is-a-canonicalized-url)
-   [Kombinieren von Basis- und relativen URLs](#combining-base-and-relative-urls)
-   [Entleeren von URLs](#cracking-urls)
-   [Erstellen von URLs](#creating-urls)
-   [Direktes Zugreifen auf URLs](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a>Was ist eine kanonisierte URL?

Das Format aller URLs muss der akzeptierten Syntax und Semantik entsprechen, um über das Internet auf Ressourcen zugreifen zu können. Kanonisierung ist der Prozess der Formatierung einer URL, um dieser akzeptierten Syntax und Semantik zu folgen.

Zeichen, die codiert werden müssen, enthalten alle Zeichen, die im US-ASCII-codierten Zeichensatz kein entsprechendes Grafikzeichen aufweisen (hexadezimale Zeichen 80-FF, , die nicht im US-ASCII-codierten Zeichensatz und hexadezimalen Zeichen 00-1F und 7F verwendet werden, bei denen es sich um Steuerzeichen handelt), Leerzeichen, "%" (die zum Codieren anderer Zeichen verwendet werden) und unsichere Zeichen (<, >, ", \# , {, }, \| , , \\ ^, ~, \[ , und \] ').

## <a name="using-the-wininet-functions-to-handle-urls"></a>Verwenden der WinINet-Funktionen zum Verarbeiten von URLs

In der folgenden Tabelle sind die URL-Funktionen zusammengefasst.



| Funktion                                                   | Beschreibung                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | Kanonisiert die URL.                             |
| [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | Kombiniert Basis- und relative URLs.                   |
| [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | Analysiert eine URL-Zeichenfolge in Komponenten.               |
| [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | Erstellt eine URL-Zeichenfolge aus Komponenten.              |
| [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | Beginnt mit dem Abrufen einer FTP-, HTTP- oder HTTPS-Ressource. |



 

## <a name="canonicalizing-urls"></a>Kanonisieren von URLs

Die Kanonisierung einer URL ist der Prozess, bei dem eine URL, die unsichere Zeichen wie Leerzeichen, reservierte Zeichen usw. enthalten kann, in ein akzeptiertes Format konvertiert wird.

Die [**InternetCanonicalizeUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) kann zum Kanonisieren von URLs verwendet werden. Diese Funktion ist sehr aufgabenorientiert, daher sollte die Anwendung ihre Verwendung sorgfältig nachverfolgen. [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) überprüft nicht, ob die an sie übergebene URL bereits kanonisch ist und dass die zurückgegebene URL gültig ist.

Die folgenden fünf Flags steuern, wie [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) eine bestimmte URL behandelt. Die Flags können in Kombination verwendet werden. Wenn keine Flags verwendet werden, codiert die Funktion die URL standardmäßig.



| Wert                     | Bedeutung                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ICU-BROWSERMODUS \_        | Codieren oder decodieren Sie keine Zeichen nach \# " " oder "?", und entfernen Sie nach "?" keine nachgestellten Leerzeichen. Wenn dieser Wert nicht angegeben ist, wird die gesamte URL codiert, und nachfolgende Leerzeichen werden entfernt. |
| \_ICU-DECODE               | Konvertieren Sie alle %XX-Sequenzen in Zeichen, einschließlich Escapesequenzen, bevor die URL analysiert wird.                                                                                                          |
| NUR \_ ICU-CODIERUNG \_ VON LEERZEICHEN \_ | Nur Leerzeichen codieren.                                                                                                                                                                                     |
| ICU \_ NO \_ ENCODE           | Konvertieren Sie unsichere Zeichen nicht in Escapesequenzen.                                                                                                                                                   |
| ICU \_ NO \_ META             | Entfernen Sie keine Metasequenzen (z.B. "." und "..") aus der URL.                                                                                                                                       |



 

Das \_ ICU-DECODE-Flag sollte nur für kanonische URLs verwendet werden, da es davon ausgeht, dass alle %XX-Sequenzen Escapecodes sind, und konvertiert sie in die vom Code angegebenen Zeichen. Wenn die URL ein "%"-Symbol enthält, das nicht Teil eines Escapecodes ist, wird sie von ICU \_ DECODE weiterhin als eins behandelt. Dieses Merkmal kann dazu führen, dass [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) eine ungültige URL erstellt.

Um [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) zum Zurückgeben einer vollständig decodierten URL zu verwenden, müssen die \_ ICU-DECODE- und ICU \_ NO \_ ENCODE-Flags angegeben werden. Bei diesem Setup wird davon ausgegangen, dass die URL, die an [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) übergeben wird, zuvor kanonisch gemacht wurde.

## <a name="combining-base-and-relative-urls"></a>Kombinieren von Basis- und relativen URLs

Ein relative URL ist eine kompakte Darstellung des Speicherorts einer Ressource relativ zu einer absoluten Basis-URL. Die Basis-URL muss dem Parser bekannt sein und umfasst in der Regel das Schema, die Netzwerkadresse und Teile des URL-Pfads. Eine Anwendung kann [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) aufrufen, um die relative URL mit ihrer Basis-URL zu kombinieren. [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) kanonisiert auch die resultierende URL.

## <a name="cracking-urls"></a>Entleeren von URLs

Die [**InternetCrackUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) trennt eine URL in ihre Komponententeile und gibt die Komponenten zurück, die durch die [**URL \_ COMPONENTS-Struktur**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) angegeben werden, die an die Funktion übergeben wird.

Die Komponenten, aus denen sich die [**URL \_ COMPONENTS-Struktur**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) zusammensetzt, sind Schemanummer, Hostname, Portnummer, Benutzername, Kennwort, URL-Pfad und zusätzliche Informationen (z. B. Suchparameter). Jede Komponente, mit Ausnahme des Schemas und der Portnummern, verfügt über einen Zeichenfolgenmember, der die Informationen enthält, und einen Member, der die Länge des Zeichenfolgenmembers enthält. Das Schema und die Portnummern verfügen nur über ein Element, das den entsprechenden Wert speichert. sie werden beide bei allen erfolgreichen Aufrufen von [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)zurückgegeben.

Um den Wert einer bestimmten Komponente in der [**URL \_ COMPONENTS-Struktur**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) abzurufen, muss der Member, der die Zeichenfolgenlänge dieser Komponente speichert, auf einen Wert ungleich 0 (null) festgelegt werden. Der Zeichenfolgenmember kann entweder die Adresse eines Puffers oder **NULL** sein.

Wenn der Zeigermember die Adresse eines Puffers enthält, muss der Zeichenfolgenlängenmember die Größe dieses Puffers enthalten. [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) gibt die Komponenteninformationen als Zeichenfolge im Puffer zurück und speichert die Zeichenfolgenlänge im Zeichenfolgenlängenmember.

Wenn der Zeigermember **NULL** ist, kann der Zeichenfolgenlängenmember auf einen beliebigen Wert ungleich 0 (null) festgelegt werden. [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) speichert die Adresse des ersten Zeichens der URL-Zeichenfolge, die die Komponenteninformationen enthält, und legt die Zeichenfolgenlänge auf die Anzahl der Zeichen im verbleibenden Teil der URL-Zeichenfolge fest, die für die Komponente gilt.

Alle Zeigermember, die auf **NULL** festgelegt sind, mit einem Memberpunkt ungleich 0 (null) zeigen auf den entsprechenden Startpunkt in der URL-Zeichenfolge. Die im Längenmember gespeicherte Länge muss verwendet werden, um das Ende der Informationen der einzelnen Komponente zu bestimmen.

Um die Initialisierung der [**URL \_ COMPONENTS-Struktur**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) ordnungsgemäß abzuschließen, muss der **dwStructSize-Member** auf die Größe der [**URL \_ COMPONENTS-Struktur**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) in Bytes festgelegt werden.

Im folgenden Beispiel werden die Komponenten der URL im Bearbeitungsfeld IDC \_ PreOpen1 und die Komponenten an das Listenfeld IDC \_ PreOpenList zurückgegeben. Um nur die Informationen für eine einzelne Komponente anzuzeigen, kopiert diese Funktion das Zeichen unmittelbar nach den Informationen der Komponente in der Zeichenfolge und ersetzt es vorübergehend durch einen **NULL-Wert.**


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a>Erstellen von URLs

Die [**InternetCreateUrl-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) verwendet die Informationen in der [**URL \_ COMPONENTS-Struktur,**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) um eine Uniform Resource Locator zu erstellen.

Die Komponenten, aus denen sich die [**URL \_ COMPONENTS-Struktur**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) zusammensetzt, sind Schema, Hostname, Portnummer, Benutzername, Kennwort, URL-Pfad und zusätzliche Informationen (z. B. Suchparameter). Jede Komponente mit Ausnahme der Portnummer verfügt über einen Zeichenfolgenmember, der die Informationen enthält, und einen Member, der die Länge des Zeichenfolgenmembers enthält.

Für jede erforderliche Komponente sollte der Zeigermember die Adresse des Puffers enthalten, der die Informationen enthält. Der Längenmember sollte auf 0 (null) festgelegt werden, wenn der Zeigermember die Adresse einer auf null endenden Zeichenfolge enthält. der Längenmember sollte auf die Zeichenfolgenlänge festgelegt werden, wenn der Zeigermember die Adresse einer Zeichenfolge enthält, die nicht auf null endet. Der Zeigermember aller Komponenten, die nicht erforderlich sind, muss **NULL** sein.

## <a name="accessing-urls-directly"></a>Direktes Zugreifen auf URLs

Auf FTP- und HTTP-Ressourcen im Internet kann direkt über die Funktionen [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) zugegriffen werden. [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) öffnet eine Verbindung mit der Ressource unter der URL, die an die Funktion übergeben wird. Wenn diese Verbindung hergestellt wird, gibt es zwei mögliche Schritte. Wenn es sich bei der Ressource um eine Datei handelt, kann sie von [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) heruntergeladen werden. Zweitens: Wenn es sich bei der Ressource um ein Verzeichnis handelt, kann [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) die Dateien innerhalb des Verzeichnisses auflisten (außer bei Verwendung von CERN-Proxys). Weitere Informationen zu [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)finden Sie unter [Lesen von Dateien.](common-functions.md) Weitere Informationen zu [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)finden Sie unter [Suchen der nächsten Datei.](common-functions.md)

Für Anwendungen, die über einen CERN-Proxy betrieben werden müssen, kann [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) für den Zugriff auf FTP-Verzeichnisse und -Dateien verwendet werden. Die FTP-Anforderungen werden so gepackt, dass sie wie eine HTTP-Anforderung aussehen, die der CERN-Proxy akzeptiert.

[**InternetOpenUrl verwendet**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) das [**HINTERNET-Handle,**](appendix-a-hinternet-handles.md) das von der [**InternetOpen-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetopena) erstellt wurde, und die URL der Ressource. Die URL muss das Schema (http:, ftp:, file: für eine lokale Datei oder https: für \[ \] \[ hypertext protocol secure) und den Netzwerkspeicherort (z. B. \] ) `www.microsoft.com` enthalten. Die URL kann auch einen Pfad enthalten (z. B. /isapi/gomscom.asp? TARGET=/windows/feature/) und Ressourcenname (z. B. default.htm). Für HTTP- oder HTTPS-Anforderungen können zusätzliche Header eingeschlossen werden.

[**InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetFindNextFile,**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)und [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (nur HTTP- oder HTTPS-URLs) können das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) erstellte Handle verwenden, um die Ressource herunterzuladen.

Das folgende Diagramm veranschaulicht, welche Handles mit den einzelnen Funktionen verwendet werden.

![Handles für die Verwendung mit Funktionen](images/ax-wnt02.png)

Das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) erstellte [**HINTERNET-Stammhandle**](appendix-a-hinternet-handles.md) wird von [**InternetOpenUrl verwendet.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) Das von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) erstellte **HINTERNET-Handle** kann von [**InternetQueryDataAvailable,**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) [**InternetReadFile,**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (hier nicht gezeigt) und [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (nur HTTP- oder HTTPS-URLs) verwendet werden.

Weitere Informationen finden Sie unter [**HINTERNET Handles**](appendix-a-hinternet-handles.md).

> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 